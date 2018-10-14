# BlockChain Technology
Blockchain Frontier Technology Tracking
> 收集前沿的区块链研究、最新项目及相关解读

## 目录
  * [前沿研究](#前沿研究)
  * [技术发展](#技术发展)
    + [共识机制](#共识机制)
    + [密码学](#密码学)
    + [博弈论](#博弈论)
    + [最新技术](#最新技术)
    + [项目介绍](#项目介绍)
  * [学习资料](#学习资料)
    + [文本资料](#文本资料)
    + [会议资料](#会议资料)
    + [开源项目](#开源项目)
    + [论坛](#论坛)
  * [商业应用](#商业应用)
  * [币圈新闻](#币圈新闻)
    + [2018.07](#2018.07)
    + [2018.08](#2018.08)
  * [投稿须知](#投稿须知)

## 前沿研究

[Gosig共识论文解读](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Gosig/Gosig%E5%85%B1%E8%AF%86%E8%AE%BA%E6%96%87%E8%A7%A3%E8%AF%BB.md) 

[Algorand论文解读](https://mp.weixin.qq.com/s?__biz=MzU3NDY2MjMwMw==&mid=2247483815&idx=1&sn=0aaea26f8b0649a6dffdfa2ee1e46501&chksm=fd2fb257ca583b41033d833726fa956cb8c92bab42a7f36c77926ed71f5073e9a743877b6988&mpshare=1&scene=1&srcid=07316xEEKDB0aFSMb97kDzIT&pass_ticket=jUns3p50ZmHAN929itla8K5XDQ%2BLxJETtR%2F15%2BCw7hY%3D#rd)  —— by 张季恒 香港科技大学教授

[PBFT vs PoA(Proof of Authority)](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/PBFT%20vs%20Proof-of-Authority%20.pdf) 将CAP定理应用到权限区块链

[From Blockchain Consensus back to Byzantine Consensus](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Blockchain%20vs%20Byzantine.pdf)

[Proof of Activity: Extending Bitcoins Proof of Work via Proof of Stake](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Proof%20of%20Activity%20Extending%20Bitcoins%20Proof%20of%20Work%20via%20Proof%20of%20Stake.pdf)

[Network Dispersity-Based Consensus Network](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Network%20Dispersity-Base%20Consensus%20Network.pdf)

## 技术发展
### 共识机制

[共识机制简介](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Technology/%E5%85%B1%E8%AF%86%E6%9C%BA%E5%88%B6%E7%AE%80%E4%BB%8B.md) 共识机制的入门资料

[共识机制中VRF的应用](https://mp.weixin.qq.com/s?__biz=MzU3NDY2MjMwMw==&mid=2247483711&idx=1&sn=9f107a9a7c8fcb34a365baf67fe80e00&chksm=fd2fb2cfca583bd9b45c508c699800f89e2bd976dab759cfb5f700c542f2c23ad3b147f57c78&mpshare=1&scene=1&srcid=0727lWK0TgX5lUDw6yVEJbdr&pass_ticket=rv7Uocqxx9gOiLNM%2Bsz0ItB6HgC%2B9grS2wKtAon83w4%3D#rd) —— by [黄祺](https://github.com/pinqy520) Mizar Network CTO

[简评6种区块链共识机制](https://www.ecommercestrategychina.com/column/review-of-the-six-types-of-blockchain-consensus-mechanism)

[新POW算法](https://blog.turtlecoin.lol/archives/introducing-cryptonight-soft-shell/)

[以太坊DPoS实现和DPoS开源分析](https://mp.weixin.qq.com/s/aTifnUB_nSWWC1pWgZIxsA)

[区块链共识的最终状态](http://medium.com/mechanism-labs/finality-in-blockchain-consensus-d1f83c120a9a)

#### Vitalik 提出一种 99% 容错的共识算法构想
[A Guide to 99% Fault Tolerant Consensus](https://vitalik.ca/general/2018/08/07/99_fault_tolerant.html) 

[Vitalik Buterin Proposes a Consensus Algorithm That Requires Only 1% to Be Honest](https://www.trustnodes.com/2018/08/10/vitalik-buterin-proposes-consensus-algorithm-requires-1-honest)

[The Byzantine Generals Problem](https://people.eecs.berkeley.edu/~luca/cs174/byzantine.pdf) Vitalik 文章中引用的论文

[拜占庭将军问题论文的中文翻译解读](https://www.jianshu.com/p/b22958a3a858)
[口头协议](https://www.jianshu.com/p/6591aea178fe)
[书面协议](https://www.jianshu.com/p/fedb160d42b3) 
[非全连接下的算法演变](https://www.jianshu.com/p/24bd8fc95feb)

[Hacker News 上的讨论](https://news.ycombinator.com/item?id=17744648)
[Reddit 上的讨论](https://www.reddit.com/r/ethereum/comments/95xwfz/a_guide_to_99_fault_tolerant_consensus_vitalik/)
[10分钟理解Vitalik说的99%容错的共识算法(视频）](https://mp.weixin.qq.com/s/J7NomklRJs_t0d0UVDmdTw)

### 密码学

The Incredible Machine (一个数独引发的惨案：零知识证明）
[英文版](http://medium.com/qed-it/the-incredible-machine-4d1270d7363a)
[中文版](http://zhuanlan.zhihu.com/p/34072069)

Zero Knowledge Proofs: An illustrated primer
第一篇：[英文版](http://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/)
[中文版](http://mp.weixin.qq.com/s/fgenZvQUjcw-rfVmtl6ryA)
第二篇：[英文版](http://blog.cryptographyengineering.com/2017/01/21/zero-knowledge-proofs-an-illustrated-primer-part-2/) [中文版](http://ethfans.org/posts/zero-knowledge-proofs-an-illustrated-primer-part-2)

[zkSNARKs in a Nutshell](http://chriseth.github.io/notes/articles/zksnarks/zksnarks.pdf)

[白话零知识证明一](http://zhuanlan.zhihu.com/p/33189921)
[白话零知识证明二](http://zhuanlan.zhihu.com/p/33307259)

[零知识证明Part1](https://ethfans.org/posts/zero-knowledge-proofs-illustrated-primer)  &
[零知识证明Part2](https://ethfans.org/posts/zero-knowledge-proofs-an-illustrated-primer-part-2)

[ZCash零知识证明](http://zhuanlan.zhihu.com/p/24440530) 极简版

[libsnark: a C++ library for zkSNARK proofs](http://github.com/scipr-lab/libsnark)

[bellman: a zk-SNARK Rust library](http://github.com/zkcrypto/bellman)

[SNARKs for C: Verifying Program Executions Succinctly and in Zero Knowledge](http://eprint.iacr.org/2013/507)

[zksnark explained](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/zksnark_explained_qap.pdf)

[Pinocchio: Nearly Practical Verifiable Computation](https://eprint.iacr.org/2013/279.pdf)

### 博弈论

[Blockchain Mining Game](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Bitcoin/BlockchainMiningGames.pdf)

[Bitcoin mining pools: A Cooperative Game Theoretic Analysis](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Bitcoin/bitcoin%E5%8D%9A%E5%BC%88%E8%AE%BA%E5%88%86%E6%9E%90.pdf)

### 最新技术

#### 闪电网络
[闪电网络优缺点介绍](https://medium.com/@argongroup/bitcoin-lightning-network-7-things-you-should-know-604ef687af5a)

[5分钟理解闪电网络](https://www.youtube.com/watch?v=rrr_zPmEiME)

[闪电网络简介](http://coincentral.com/lightning-network-beginners-guide/)

[State Channel Applications（状态通道应用](http://medium.com/statechannels/state-channel-applications-1f170e7d542e)

#### 侧链
[状态通道和侧链的区别](http://hackernoon.com/difference-between-sidechains-and-state-channels-2f5dfbd10707)

#### 分片
[分片设计哲学](https://ethfans.org/posts/sharding-design-philosophy) Vitalik 为 IC3 作的关于分片的演讲

[Provisioning Sharding for Smart Contracts: A Design for Zilliqa](http://blog.zilliqa.com/provisioning-sharding-for-smart-contracts-a-design-for-zilliqa-cd8d012ee735) Zilliqa 的智能合约分片设计 

#### 其他
[三分钟了解隔离见证](https://zhuanlan.zhihu.com/p/32613487) 

[公有链的最新挑战Part1](https://ethfans.org/posts/fundamental-challenges-with-public-blockchains-part-1) &
[公有链的最新挑战Part2](https://ethfans.org/posts/fundamental-challenges-with-public-blockchains-part-2)

[探讨以太坊的短期扩展解决方案 英文版](https://medium.com/web3foundation/investigating-short-term-scaling-solutions-for-ethereum-a5951fee8967) [中文版](https://ethfans.org/posts/investigating-short-term-scaling-solutions-for-ethereum)

[以太坊横向扩容方案](http://ethfans.org/posts/ethereum-scaling-solutions-and-tradeoffs)

### 项目介绍

[初链黄皮书解读]( https://github.com/codereba/simpleai/blob/master/TrueChain.md)

[Nervos白皮书](https://github.com/NervosFoundation/binary/tree/master/whitepaper)

[对话Nervos](https://mp.weixin.qq.com/s/giniWFxxAFGT0fr2qbZc_Q)

[状态通道智能合约：终极安全钱包](https://medium.com/stk-token/state-channels-the-ultimate-secure-wallet-9a17da38bd77)

[深入Geth理解为啥同步以太坊节点这么慢](https://hackernoon.com/getting-deep-into-geth-why-syncing-ethereum-node-is-slow-1edb04f9dc5)

[Ioex访谈录](https://mp.weixin.qq.com/s/VD9qbMqEN_YZt6e309nltw)  物联网领域项目

[Celer Network 访谈](https://mp.weixin.qq.com/s/mLptSJQKoSVQpGd3VLx1Fw)  Google背景团队，链下操作系统，快速确认闪电网络

[Neo的新路线图旨在为智能合约的未来充电](https://dailyhodl.com/2018/08/07/neos-new-roadmap-aims-to-supercharge-the-future-of-smart-contracts/)

[通过链上智能合约验证 Plasma 网络的链下状态](https://ethresear.ch/t/off-chain-plasma-state-validation-with-on-chain-smart-contract/2813)

[Kyber Network 的最新进展](https://blog.kyber.network/community-and-ecosystem-updates-growing-the-decentralized-ecosystem-9a096a9205ef)

[Kademlia协议](https://zhuanlan.zhihu.com/p/38425656) IPFS在使用的全球分布的DHT（分布式哈希表）协议

[Cosmos跨链详解](http://zhuanlan.zhihu.com/p/42693285)

[A Deep Look Into Cosmos — the Internet of Blockchains (深入探索 Cosmos)](http://medium.com/@juliankoh/a-deep-look-into-cosmos-the-internet-of-blockchains-af3aa1a97a5b)

[使用新的 Scilla IDE 创建 Zilliqa 的智能合约](http://blog.zilliqa.com/budil-savant-ide-566cf6d50c07)

## 学习资料
### 文本资料
[比特币白皮书 英文版](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Bitcoin/bitcoin_en.pdf) [中文版](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Research/Bitcoin/bitcoin_cn.pdf)

[Mastering Bitcoin 英文版](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Book/Mastering%20Bitcoin.pdf) [中文版](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Book/Mastering%20Bitcoin%20%E4%B8%AD%E6%96%87%E7%89%88.pdf) 

[Mastering Bitcoin 2nd Edition](https://github.com/bitcoinbook/bitcoinbook)

[比特币与数字货币技术](https://www.coursera.org/learn/cryptocurrency) Coursera上普林斯顿大学的公开课，后续会整理中文版笔记

[BlockChain Blueprint for a New Economy](https://github.com/sarah21cn/BlockChainTechnology/blob/master/Book/blockchain%20blueprint%20for%20a%20new%20economy.pdf)

[zastrin关于Ethereum智能合约开发](https://cn.zastrin.com/)

[比特币Transaction入门](https://klmoney.wordpress.com/bitcoin-dissecting-transactions)

[比特币开发指南 英文版](https://bitcoin.org/en/developer-guide)  [中文版](https://www.yiyibooks.cn/Gamma/bitcoin/developer-guide.html)

[BlockChain教程](https://liuchengxu.gitbooks.io/blockchain-tutorial/content/) 包括Bitcoin，Ethereum，IOTA等项目解读 —— by [Liuchengxu](https://github.com/liuchengxu)

[EthFans Wiki](https://github.com/EthFans/wiki/wiki)

### 会议资料
[BCCon 区块链大会 PPT 合集 ](https://ppt.geekbang.org/list/bccon2018?device=geekTime.ios&from=groupmessage&isappinstalled=0)

### 开源项目
#### BlockChain
[Go-Ethereum](https://github.com/ethereum/go-ethereum) Go语言实现的官方库

[Ethereum Casper](https://github.com/ethereum/casper) Casper实现

[NEO](https://github.com/neo-project/neo) NEO项目源码

[EOS](https://github.com/EOSIO/eos)  EOS项目源码

[Cardano](https://github.com/input-output-hk/cardano-sl) Cardano项目源码

[XDAG Dagger](https://github.com/XDagger/xdag) 首个可以挖矿的DAG项目

[IPFS](https://github.com/ipfs/ipfs) IPFS项目源码

[Go语言的BlockChain实现](https://github.com/Jeiwan/blockchain_go)

[Java语言的BlockChain实现](https://github.com/wangweiX/blockchain-java) 模仿上一个项目的思路，使用Java语言实现

[Khipu](https://github.com/khipu-io/khipu) 基于 Scala/Akka 实现的 Ethereum 协议客户端

#### Consensus Algorithm
[HoneyBadgerBFT实现](https://github.com/amiller/HoneyBadgerBFT)

[DPos+PBFT实现](https://github.com/sqfasd/dpos-pbft)

### 论坛
[bitcointalk网站](https://bitcointalk.org/)

## 商业应用

[一文详解证券型代币全生态](https://www.chainnews.com/articles/771233044827.html)

[看AVINOC如何将区块链技术带入商用航空业](https://coinidol.com/hong-kong-startup-avinoc-to-bring-blockchain-innovation-to-business-aviation/)

[区块链技术改造房地产行业](https://blockchainreview.io/blockchain-in-real-estate-property-sector/)

[区块链在游戏领域的使用场景和挑战]( https://www.youtube.com/watch?v=K1BUdwC5Vo0&feature=youtu.be )

[区块链助力传统资产交易](https://hackernoon.com/traditional-assets-not-getting-sold-look-towards-blockchain-for-an-answer-d884d23c3aa5)

[利用区块链技术对抗虚假新闻传播](https://cryptodisrupt.com/blockchain-technology-to-stop-fake-news/)

[区块链和用户数据隐私](https://cryptodisrupt.com/blockchain-and-the-battle-for-user-data/)

[新的扑克牌游戏](https://www.reddit.com/r/BlockChain/comments/9735dh/new_crypto_poker_application_playing_with_eth_or/)

[区块链如何影响供应链行业](https://hackernoon.com/how-is-blockchain-disrupting-the-supply-chain-industry-f3a1c599daef)改进货物从生产者到消费者的流动

[区块链金融应用大趋势](http://www.envisioninteligence.com/industry-report/global-fintech-blockchain-market/?utm_source=redit-anusha)

## 链圈新闻
### 2018.07
[Hodl加密货币投资策略](https://dailyhodl.com/2018/07/22/the-hodl-investment-strategy-from-bitcoin-to-altcoins/)

[加密货币利好？G20 官方表示加密货币为金融系统和世界经济环境带来“显著的促进效益” ](https://dailyhodl.com/2018/07/23/breaking-g20-says-cryptocurrency-can-deliver-significant-benefits-to-financial-system-and-worldwide-economy/)

[Google上线区块链云服务](http://cryptocoinjunky.com/google-announces-blockchain-as-apart-of-cloud-services/)

[AI & Blockchain: An Introduction]( http://mattturck.com/ai-blockchain/) 探索AI如何和区块链结合？区块链是否可以解决当前 AI 所面临的数据以及算力的问题？

[Cryptocurrencies are money, not equity（加密货币是钱不是资产）](https://tokeneconomy.co/cryptocurrencies-are-money-not-equity-30ff8d0491bb)

[IBM携巴克莱银行和花旗集团等9个金融机构建立基于区块链技术的应用商店](https://www.cryptocurrencyguide.org/ibm-barclays-and-citigroup-are-building-a-blockchain-based-app-store/)

[XAIN Vehicle Network——保时捷成为第一个将区块链技术应用到车载系统的传统汽车制造商](https://medium.com/@XAIN/part-1-technical-overview-of-the-porsche-xain-vehicle-network-f70bb117be16)

### 2018.08
[使用区块链技术保存电子健康记录](http://www.sbrc2018.ufscar.br/wp-content/uploads/2018/04/07-181717-1.pdf)

[我们已经知道的区块链杀手级应用](https://hackernoon.com/we-already-know-blockchains-killer-apps-f2d443eba35)

[泰国最大的连锁电影院接受数字加密货币](https://www.ccn.com/thailands-largest-movie-theater-chain-will-accept-cryptocurrency/)

[数据库还是区块链](http://go.bftf.io/blog.amalto.com/blog/blockchain-network-or-conventional-database)

[Blockchain Platforms: One Chain to rule them all?（区块链平台：一链统治全世界？）](http://hackernoon.com/blockchain-platforms-one-chain-to-rule-them-all-f3f7dda84bae)

[The Store of Value Thesis（价值存储的理论](http://tokeneconomy.co/the-store-of-value-thesis-42d3cfde50a9)

[A deductive valuation framework for cryptocurrencies加密货币的演绎评估框架)](http://medium.com/@alexander.liegl/a-deductive-valuation-framework-for-cryptocurrencies-a6bfa085a8b6)
作者提出了一个思维框架，分为 12 个层级，来分析和评估加密货币的价值。

[Democracy on the Blockchain: Incentivizing Voter Participation through Cryptoeconomics（区块链上的民主：通过加密经济学激励选民参与）](http://btcmanager.com/democracy-blockchain-incentivizing-voter-participation-cryptoeconomics/)
民主是否也可以通过经济激励来进行？这篇文章总结了学者在这个领域的研究结果。

[Blockchain vs DApp](https://hackernoon.com/blockchain-vs-dapp-af62261dd721)

[智能合约的入门指南](http://hackernoon.com/everything-you-need-to-know-about-smart-contracts-a-beginners-guide-c13cc138378a)

[DHT分布式Hash表](http://colobu.com/2018/03/26/distributed-hash-table/) 老文章，但整理的还是比较全面

[UTXO 和 Account 模型对比](http://mp.weixin.qq.com/s/2JAD-Q2NU2Q_SS9xtRVK9A)

[BigQuery中的以太坊：用于智能合约分析的公共数据集](http://chinagdg.org/2018/08/ethereum-in-bigquery-a-public-dataset-for-smart-contract-analytics/)

### 2018.09
[理解证券型代币 (Security Token)和实用型代币 (Utility Token)的不同](https://thecoinoffering.com/learn/security-tokens-vs-utility-tokens/)

### 2018.10
[Scaling Bitcoin 东京区块链会议结束，有视频回放](http://tokyo2018.scalingbitcoin.org/)

[Cryptonetworks and the Theory of the Firm (加密网络与企业理论)](http://medium.com/@QwQiao/cryptonetworks-and-the-theory-of-the-firm-a11961a41f7c)
 
[STO的潜力在哪](http://mp.weixin.qq.com/s/Ymfd9uwUEkKNP8PfzAnGQA)

[需要了解的加密货币概念汇总](http://medium.com/coinmonks/cryptocurrency-lingo-cheat-sheet-crypto-terms-you-need-to-know-42abc0db6fc6)

## 投稿须知
欢迎大家踊跃投稿，投稿前请先阅读[投稿须知](https://github.com/sarah21cn/BlockChainTechnology/blob/master/ContributionGuidelines.md)
