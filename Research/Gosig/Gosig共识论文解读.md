### Gosig共识论文解读

#### Abstract

BFT在联盟链中应用广泛，但是也存在两点问题。 Gosig：

- 基于密码学的leader选举 VRF
- 协议层的多轮投票，如基于Gossip的消息传播的层次优化（分层？）
- 性能：

> Gosig guarantees safety even in a network fully controlled by adversaries, while providing provable liveness with easy-to-achieve network connectivity assumption. On a wide area testbed consisting of 140 Amazon EC2 servers spanning 14 cities on five continents, we show that Gosig can achieve over 4,000 transactions per second

#### Introduction

- 区块链

> 由于比特币的兴起，越来越多的人们关注到区块链的底层技术。区块链使用分布式的分类账来记录交易，具有full decentralization, offline-verifiability, and most importantly, scalable Byzantine fault tolerance on the Internet.

- 应用领域

> payment services, logistics, healthcare, and Internet-ofThings

- 前提条件

> 比特币不需要许可即可加入。我们主要致力于联盟链，所以需要进行离线身份验证(offline authentication)才能加入。这对很多商业应用都有利。而且我们不需要考虑女巫攻击（Sybil attacks）

- 与传统的分布式事务处理系统相比，区块链面临的挑战

1. 用户之间不能相互信任，拜占庭失败非常常见。所以我们不能依靠一个小的法定人数，如(Chubby或ZooKeeper）达成共识。所以只能依赖拜占庭共识。
2. 系统在开放的互联网上运行，网络存在延迟。且因为参与者地址公开，所以攻击者可以针对某些节点进行攻击，如DDOS。甚至可以对leader节点进行适应性攻击。
3. 人们希望联盟链提供more traditional transaction semantics，much higher throughput and lower latency than Bitcoin。

- 现有的BFT算法问题

> 无法解决Leader节点自适应攻击。即使他们会按照固定的顺序更新Leader节点。

- 现有解决方案

1. Algorand通过隐藏Leader身份来避免攻击。避免了Leader节点自适应攻击
2. ByzCoin结合PoW，采用基于多重签名的PBFT。提供了可扩展性。
3. HoneyBadgerBFT采用异步原子广播和异步通用子集（ACS）。容忍任意网络故障。
4. Adardvark使用性能指标来除法师徒更改合Spinning
5. Tendermint通过循环方式来切换领导人

- Gosig优点

1. 结合以上三个协议(1,2,3)的优点，即使在部分同步网络下也有效
2. 网络层优化：使用Gossip网络

- 理论结果

> 确保所有区块链副本都相同，同时减少分叉

- 实验结果

> 基于140台亚马逊EC2，覆盖了世界五大洲的14个城市。实验验证可以实现4000TPS的吞吐量，平均交易确认延迟1分钟。即使有1/4的节点失败，页可以保持在超过3500的TPS。

#### Problem Definition and Assumptions

- 前提条件

1. 强大的密码学和PKI。我们只考虑联盟链，并且用一个trusted public key infrastructure (PKI)来验证用户身份
2. 异步网络的安全。我们的协议可以在异步网络条件下标尺安全，这意味着消息可以被任意删除、重新排序或重复。
3. 在部分同步网络下也适用。
4. 部分同步时钟，使用standard Network Time Protocol(NTP)实现

##### Overview 正常流程

1. 用户会对区块进行验证。放弃一个无效的区块和交易，并将发起人加入黑名单
2. 每一轮30s，包含Leader选举和BFT共识

- Leader选举：Leader在本地进行选举，身份只有自己知道。当充分履行完Leader的职责之后，身份才会被别人发现。

> At Stage I, a selected potential leader packs nonconflict uncommitted transactions into a block proposal, disseminates it with gossip, and acts just like a normal node afterwards. Note that a potential leader’s identity can only be discovered by others (including the adversary) after she has full-filled her leader duties

- BFT共识：每轮会对一个区块达成共识。如果一个用户同意一个区块，就将他的签名加入P message中，并且发送出去。当收到关于一个区块的P message包含至少2f+1个签名时，用户开始发送TC message。当收到超过2f+1个TC message之后，用户会将该区块写入本地区块链中。

##### Detail 考虑异常情况

###### 用户本地状态

> 每个用户都可以看做一个有限状态机。每个用户都会保存一个本地状态，并且根据这个状态决定下一步的操作。本地状态是一个四元数组。Broot, hroot, Btc, F。

- Broot: 上一个区块 hroot：上一个区块的高度
- Btc：当前未决区块 F： Btc的及时性？

> 除了出现在元组中的元素之外，pi也是隐含地维护两个变量：croot和ctc。 croot是 证明Broot有效性的承诺证书，ctc是Btc的提案证书。

###### Leaer选举

> Leader选举是每一轮的第一步。目的是秘密随机地选取出Leader节点。最大的挑战是在Leader节点发出PR Message之前，让选举结果不可预测。

###### Leader打包块

> 打包完成后，对当前包进行签名，然后将当前的块提议放在PRMessage中

###### 第一阶段：区块广播

> 所有Leader节点将提出的区块尽可能多的发送给诚实参与者。其他参与者会转发收到的所有有效区块（PRMessage）。同一轮中可能有多个区块，因为可能有多个Leader节点，或者恶意Leader节点故意提出多个区块。

###### 第二阶段：签名收集

> 每轮会对一个区块达成共识。如果一个用户同意一个区块，就将他的签名加入P message中，并且发送出去。当收到关于一个区块的P message包含至少2f+1个签名时，用户开始发送TC message。当收到超过2f+1个TC message之后，用户会将该区块写入本地区块链中。

###### 多重签名

1. 多重签名两种方法优劣
2. 签名聚合，缩小签名的存储空间

> 1000个用户使用2048比特签名，他会占据256KB的空间来存储数据。如果使用签名聚合，只需要4256bytes，1/60原来所占和空间的大小、

###### 离线恢复策略

> 正常情况下，区块和签名会被广播到所有的用户。如果一个用户在第r轮离线，未收到本轮快的信息。可以在后续轮实现恢复。

1. 如果用户收到第r轮的足够签名，但是没有收到区块。他会尝试从其他已签名过改区块的的用户请求获取当前区块。
2. 如果用户离线一段时间，他会去获取所有的区块和证明。区块是offline-verifiable，从任何用户处获取到的具有有效签名的区块都是被验证过的。

#### 安全分析引理

我们可以证明Cosig在完全异步的情况下，可以提供安全性 引理：

1. 如果一个诚实的节点第r轮在高度h提交一个区块B，其他节点就不能提出高度h` <= h 的块。
2. 第r+1轮提出的区块的高度h = hroot + 1

#### 实施层优化

1. 异步发送交易和区块

> message只包含区块的哈希值。交易信息会通过gossip协议异步发送给所有用户，独立于共识过程。当玩家未收到原始交易信息，而需要对块做出决议时，可以从其他用户出检索当前的交易信息。

1. 第二阶段持续的Gossip协议通信
2. 断开连接的节点会被加入本地黑名单，知道重新收到该节点的消息为止
3. 使用LIFO栈结构来存储待处理的消息。消息的到达速度可能超过节点的处理速度，使用栈结构是因为后续到达的消息通常会包含更多的签名信息。
4. 防止签名溢出。对于伪造的超长的签名，用户不进行处理。

#### 实现

- 使用JPBC库来实现密码学计算。使用grpc-java来进行网络通信。大约5000行代码
- 测试平台。区域内网络延时小于1ms，网络带宽大约100MBps。区块间带宽在2-30之间。

> We believe the testbed is a good emulation of a typical multi-datacenter WAN.

- 核心参数：回合时间 & 最大块大小
- 只传播块哈希值，减小块大小

#### 实验结果

> 可调整参数： 块大小、用户数、故障节点数，每轮时间

- TPS

1. TPS - Latency 35个用户，TPS可以到6000，140个用户，TPS可以到4000.
2. 块大小 - TPS 限制在4MB，可以达到理论4000TPS
3. N=140 f=35 TPS减少10%左右
4. 每轮时间由30s变成10s， TPS变小

- 每阶段耗时

> 阶段I 比 阶段II 更耗时。

- 可扩展性 主要考察第二阶段，因为第一阶段和其他的Gosip网络没有差别。 考察参数调整对TPS和时延的影响。发现可以达到一个平衡。

#### 参考文献

1. <https://blog.csdn.net/lemongirls/article/details/80238790>