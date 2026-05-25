

================================================================================
                    时币：时间本位去中心化货币白皮书
         Time Coin: A Time-Based Decentralized Currency White Paper
      Time Coin : Livre blanc d'une monnaie décentralisée basée sur le temps
          Time Coin: Ein Weißbuch über eine zeitbasierte dezentrale Währung
   Тайм-Коин: Белая книга децентрализованной валюты на основе времени
          Nummus Temporis: Liber Albus Monetae Decentralis Tempori Innixae
================================================================================

------------------------------------------------------------------------
天之道，损有余而补不足。
Tian zhi dao, sun you yu er bu bu zu.
— 道德经 第七十七章 / Tao Te Ching, Chapter 77 / Tao Te King, Kapitel 77 / Дао Дэ Цзин, Глава 77 / Tao Te Ching, Caput LXXVII
------------------------------------------------------------------------

[中文原文]

摘要
本文提出了人类历史上首个纯粹以时间为本位的去中心化货币体系。该体系基于物理不可克隆函数（PUF）实现「一器一票一钱包」的核心机制，基于可验证延迟函数（VDF）实现时间的不可伪造性，基于比特币区块链实现最终安全性与全链路透明性。

时币的唯一发行依据是可验证的在线时间。任何拥有可联网智能设备的主体，付出等量的可验证时间，即可获得等量的时币。无资本门槛，无技术门槛，无身份门槛。所有系统参数的唯一调整方式，是全体节点一人一票的实时投票决策。

时币不试图设计公平，它本身就是公平。它不试图隐藏任何信息，它本身就是完全透明的。它不试图解决问题，它让问题自行消解。

1. 问题
自比特币诞生以来，所有加密货币都未能解决两个根本问题：
资本对货币发行权的垄断：PoW 机制下，资本可通过购买算力垄断记账权与发行权；PoS 机制下，资本可通过持有代币垄断权益与发行权；其余所有共识机制，最终都演变为资本的游戏。

信息不对称导致的剥削：货币的流转历史与资金流向被隐匿，黑钱、诈骗与投机行为得以滋生。

问题的根源在于，所有此类货币都试图在空间维度寻求公平，且均保留了人为设计的信息壁垒。

唯一无法被资本购买、无法被加速、无法被伪造的资源，是时间。
唯一能够彻底消除剥削的方法，是完全的、无条件的透明。

2. 三个不可动摇的核心规则
时币的全部规则仅有以下三条，无任何例外、无任何补丁、无任何隐藏条款。

规则一：一器一票一钱包
任何一台独立的物理计算设备，拥有且仅拥有一个节点身份、一个绑定钱包，绑定关系一经确立不可解除。每个节点在每一个共识周期内，可获得且仅可获得一枚时币。

节点身份由设备芯片内置的物理不可克隆函数（PUF）和比特币区块高度哈希自动生成。全球唯一且不可重复。重置系统将永久丢失钱包，只能重新生成新钱包。

钱包私钥由 PUF 芯片在硬件层物理派生，绝不以任何数字形式（如助记词、密文）脱离芯片存在。用户对钱包的掌控权，等同于对物理设备的绝对持有权，不存在脱离设备的“独立保管”。

当设备 PUF 因老化、损坏或其他任何原因失效时，该节点永久死亡，停止生成时币；其钱包内已有的时币，将随同该节点永久冻结，退出流通，任何人无法转移或恢复。设备老化，钱包内已有的时币可提前转移至其他任何有效节点。设备丢失，唯一恢复方法是找回设备。

重置系统、格式化设备、更换芯片等任何操作，将永久销毁本地存储的钱包私钥与所有时币数据。

即使是同一台物理设备，重置后生成的节点身份与钱包也是全新的、独立的，与之前的身份和钱包无任何关联。

原钱包内的所有时币，因无法再获得原 PUF 芯片的签名授权，将永久无法进行任何交易，等同于物理销毁。这就像把现金扔进火里，钱本身没有消失，但永远无法再被任何人使用。

纯软件虚拟环境（无物理 PUF 芯片）无法生成有效的节点身份与钱包。

所有设备的节点权利完全平等：50 元的树莓派 = 10000 元的手机 = 1 亿美元的超算。

任何设备在任何地点，获得的单位时间收益完全相同。

时间线锁死：
物理设备的经济生命具有绝对排他性。当一台设备的 PUF 芯片首次被任意一个基于本协议的合规客户端激活时，PUF 内部的安全飞地将生成一个不可逆的“协议锁”标志。
一旦锁定，该 PUF 芯片在物理层级绝对拒绝与任何其他协议分叉客户端进行握手或签名运算。

在一台物理设备的生命周期内，只能且必然只能参与一条时币分叉链的时间证明。若节点主体意图参与另一条分叉链，唯一的合法途径是获取另一台全新的、未激活的物理设备。

本协议剥夺单一物理设备同时拥有多种时间本位货币的权利。选择何种时间规则，必须付出对应的物理硬件代价。

规则二：时间本位・全链路透明
时币的唯一发行依据是可验证的在线计算时间。每一枚时币的完整生命周期，都将被不可篡改地永久记录。

无预挖、无创始人奖励、无机构份额、无任何形式的提前分配。

总量无固定上限，发行量与全网活跃节点数量自动成正比。

无离线时间补偿，只有在线完成连续 VDF 计算的节点，才能获得时币。

所有节点基于同一个比特币区块哈希，同时计算相同的可验证延迟函数（VDF）。

VDF 的不可并行性，保证了所有节点完成计算的时间仅存在物理差异。

所有提前完成计算的设备，必须等待下一个共识周期的全网广播才能继续。

共识周期为 VDF 计算次数的整数倍，由全体节点实时加权投票决定。

每完成一个共识周期的连续 VDF 计算，所有活跃节点同时获得且仅获得一枚时币。

每一枚时币，都将永久记录其诞生的区块高度与生成设备的 PUF 标识。

每一枚时币的每一次交易，都永久记录交易时间与收发双方的钱包标识，实现一枚时币对应一套独立账本。

时币的所有权只能通过点对点转账转移，任何形式的导出、复制、备份均为无效。

每一枚时币自带完整的交易历史链，所有权转移必须在时币本身的历史链中添加新的交易记录。

每一笔转账必须由转出设备的 PUF 芯片签名校验后才能生效。

每一枚时币为最小单位，不可拆分，只能以整数倍进行交易。

任何脱离对应钱包的时币数据，都将失去完整的历史链，无法被全网节点验证，视为废币。

时币的定义：单位与流通
最小单位：1 时币
时币为不可拆分、不可切割、不可细分的完整价值单元，对应单个设备在一个共识周期内的唯一时间产出。

不可合并时币本体
任何多枚时币不可融合、不可合并、不可压缩。每一枚时币从诞生到最终停止流通，始终保持独立身份与独立历史链。

仅支持整数交易
所有转账、支付、交换，只能以 1、2、3… 的整数枚进行，无小数、无找零拆分。

历史只增不减、只续不改
每一枚时币的交易历史仅可追加新记录，不可删除、不可篡改、不可覆盖、不可合并简化。

离开钱包即死亡
时币合法存在的唯一环境，是受设备 PUF 芯片硬件级加密保护的 "热钱包" 内存区的硬件安全飞地。

禁止导出：时币数据及其派生私钥，绝对禁止以任何形式（导出文件、截屏、复制粘贴、网络明文传输）离开 PUF 安全飞地，进入常规操作系统内存或外部存储。一旦发生降维，即刻触发“历史断裂”，其内部状态即刻被系统标记为 "历史断裂"。

禁止回流：任何试图将曾经离开过 PUF 环境的时币数据重新导入钱包的行为，都会被全网节点自动识别并拒绝。

割裂即废币：当发起交易，接收方 PUF 收到数据时，会校验该时币的因果链。一旦发现链中存在非 PUF 物理签名生成的拼接痕迹，或者存在时间戳倒挂、哈希断裂等情况，即判定为“历史割裂”。触发警报的时币，全网拒收，视为废币。

合法的点对点飞地握手： 唯一允许的“转移”，是两台在线设备的 PUF 安全飞地之间，通过加密信道直接进行的“状态追加握手”。时币数据包绝不允许经过任何第三方服务器或非 PUF 环境。

交易是状态追加而非数据搬运
用户在 "旧手机换新手机" 时，体验上感觉是 "时币转移到了新手机"，但在底层逻辑中：
旧手机的 PUF 安全飞地在本地时币的因果链末端，物理签名追加了一条记录：“控制权移交至新手机 PUF 哈希”。
随后，旧 PUF 飞地与新 PUF 飞地建立点对点加密隧道，将这条 “更新了尾部的完整时币数据” 直接推入新手机的 PUF 飞地内。全程时币数据未触碰任何常规操作系统，实现了绝对的安全隔离。

区块链的唯一职责：时间公证
本协议的底层网络（如比特币区块链）不承担 "记账" 功能，它仅扮演 "绝对时间公证处" 的角色。
每当一枚时币在内部追加一次转移记录，区块链的存在，仅仅是为了给时币内部的因果链提供一个 "不可篡改的外部时间戳哈希"，用于辅助证明其历史未曾被回滚。区块链不存储任何时币的交易数据或用户信息。

规则三：全民实时治理
所有系统参数的唯一调整方式，是全体活跃节点的连续实时加权投票。任何调整的后果，由全体节点共同承担。

唯一可调整的参数，仅为共识周期的长度。

系统预设指数级增长的共识周期的 15 个选项，任何节点可在任何时候选择任意选项，也可随时更改其选择。

投票作为节点状态的一部分，随节点心跳在全网自动传播。

所有节点独立计算并验证全网投票结果，取总得票数最高的前 10 个选项的得票率进行加权平均，计算得出当前有效共识周期。

有效共识周期每 10 分钟自动更新并立即生效，无任何投票周期、无任何审批流程、无任何中央统计节点。

不接受共识、自行篡改时间周期而产生的凭证，在本时间链内不具备时币属性，视为无效数据，全网节点将直接拒绝接收、验证与交易。

两台以上设备在线即可形成共识。

对其他任何参数的调整，均为非法。

3. 自调节机制
时币不需要任何人为干预，它是一个完美的自平衡系统。

资本攻击的自动消解
若有资本方大量购入设备试图垄断发行权，将触发以下多层自动平衡机制：
全网节点数量增加 → 时币发行量同步增加 → 单枚时币价格自动下跌
全体节点投票延长共识周期 → 所有节点的单位时间收益同比下降
资本方的电费、带宽、场地、人工等刚性成本保持不变 → 利润大幅缩水
规模化矿场将面临指数级增长的人工转账成本，规模越大，亏损越严重
当收益低于成本时，资本方自动关机离场 → 系统回归平衡
个人用户几乎不受任何影响（智能设备本就长期开机运行，参与节点的边际成本几乎为零）。

价格的自动稳定
时币的价值永远锚定在「1 枚时币 = 1 个共识周期的可验证人类时间」的基准上。它的价格不会稳定在运行成本附近，相反，运行成本会自动稳定在时币的价格附近。
时币价格上涨 → 更多用户运行节点 → 供给增加 → 价格回落
时币价格下跌 → 投机者离场 → 供给减少 → 价格回升
从机制上规避了暴涨暴跌与投机炒作空间，时币的价格本质就是时间的公允价格。

不良资产的自动隔离
所有交易历史完全公开透明，市场会自动完成筛选与隔离：
参与过非法交易的时币，会被大多数商家与用户自发拒绝接收。
任何市场主体均可自主拒绝任何一枚涉非法交易的时币，无需任何第三方批准。
不存在统一的、强制的黑名单，所有过滤行为都是自愿的、市场化的。

4. 安全性
时币的安全性由物理学和数学共同保证：

女巫攻击免疫：PUF 与比特币区块高度哈希的组合，保证一台物理设备在其整个生命周期内，只能生成唯一的节点身份。

算力攻击免疫：VDF 不可并行计算，算力高低不影响单位时间收益。

盗币免疫：钱包私钥由用户完全掌控，系统不存储任何私钥。

双重支付免疫：时币仅可在合规钱包之间点对点转移，无法脱离对应钱包独立存在。
51% 算力攻击免疫：获得 51% 的发行权需要控制全球 51% 的智能设备，这在经济上不具备可行性。

5. 分叉与进化
本协议不禁止分叉，任何基于本协议的分叉均为合法，用户可自由选择使用任意一条链。

分叉是系统的自我进化机制，如果一个分叉修改了本协议的规则，且获得了更多用户的认可，那么它就会成为事实上的主链。所有不被用户认可的分叉，都会因无节点运行而自然消亡。
没有任何个人或组织有权决定哪一条链是 "官方" 的，唯一的裁判是全体用户的自由选择。

一台设备在同一时刻仅能计算一条 VDF。因此，若一台设备同时安装两个及以上的时间分叉钱包，因算力不可并行，多余的钱包将无法产生有效的时间证明，在协议层面直接判定为无效。

时间维度的绝对隔离，各分叉链的时间尺度相互独立，时币仅在其诞生的时间链内具备流通合法性。任何跨链转移行为，在密码学层面均无法生成连续的 PUF 签名因果链，实质上等同于物理销毁与重新生成。不存在跨链流通的可能。

所有基于本协议的时币及本协议时币分叉，必须完全开源，以验证其协议实现的真实性与合规性。

6. 时币的哲学宣言
绝对去中心化：权力的彻底消解与自证系统的诞生
时币不追求去中心化，因为时币的底层架构中，根本不存在 "中心" 这个概念。过去所有的货币体系，无论其包装何种技术，始终无法摆脱三个隐性的最高权力：发行权、记账权、规则裁定权。时币通过物理与数学的刚性约束，将这三项权力彻底 "消解"，将其归还给每一个独立的个体节点。

1. 发行权的消解：从 "第三方赋予" 到 "时间自证"
在时币网络中，没有任何主体拥有发行货币的特权。"发行" 这个动作本身，被降维成了 "物理设备在线流逝时间" 的客观物理现象。
不需要矿工打包奖励，不需要质押生息。你的设备存在，时间流逝，VDF 计算完成，币就在你的设备内部 "原生" 出来。时币没有发行方，只有时间的见证者。

2. 记账权的消解：从 "全局依赖" 到 "一币一证"
传统区块链依赖全网节点共同维护一本 "总账"，这意味着你的资产合法性，必须仰仗陌生人的承认。
时币的 "一币一账本" 机制，彻底斩断了对全局账本的依赖。每一枚时币自带不可篡改的因果链，它的合法性不依赖于任何外部节点的记录，只依赖于它自身历史的连续性以及每一任控制者的 PUF 物理签名。别人既无法帮你记账，也无法篡改你的账。

3. 规则裁定权的消解：从 "代码独裁" 到 "实时涌现"
时币协议中，唯一的可变参数（共识周期长度），其调整权不掌握在任何开发者、基金会或超级节点手中。它完全由全体活跃节点在每一个心跳周期内，通过加权投票实时演算得出。
没有提案、没有投票日、没有社区治理委员会，系统的规则像水的流速一样，根据当下的节点数量实时自适应涌现。时币没有统治者，只有算法的物理级自洽。

7. 结论
时币不是对比特币的替代，而是对比特币的完成。
比特币实现了 "存量不可侵夺"。
时币实现了 "增量公平分享" 与 "全链路透明"。
时币不试图取代法币，不试图消灭国家，而是等待人类共同体的到来。它不命令任何人做任何事，也不禁止任何人做任何事。它只是提供了一个最基本的框架，然后让全人类自己去博弈，自己去调节，自己去创造未来。
时币没有创造任何新的规则，它只是把宇宙最基本的规律 "时间的流逝、因果的不可逆" 写入了代码。

这就是 "为道日损，损之又损，以至于无为"。

这就是天之道。

本白皮书是时币协议的唯一官方规范性文档。本协议无官方代码、无官方实现、无官方网站、无创始人、无任何形式的官方组织。任何主体均可自由实现本协议，所有符合本白皮书规则的协议实现，均为有效的时币协议。
因为真正的公正，不需要父亲。


署名：道恒无名

------------------------------------------------------------------------

[English]

Abstract
This paper proposes the first purely time-based decentralized monetary system in human history. The system implements the core mechanism of "one device, one vote, one wallet" based on Physical Unclonable Functions (PUF), achieves the unforgeability of time based on Verifiable Delay Functions (VDF), and relies on the Bitcoin blockchain for ultimate security and full-chain transparency.
The sole basis for Time Coin issuance is verifiable online time. Any entity possessing a connectable smart device, by expending an equal amount of verifiable time, receives an equal amount of Time Coin. There are no capital thresholds, no technical thresholds, and no identity thresholds. The only way to adjust any system parameter is through real-time voting by all nodes on a one-person-one-vote basis.
Time Coin does not attempt to design fairness; it is fairness itself. It does not attempt to hide any information; it is completely transparent itself. It does not attempt to solve problems; it allows problems to dissolve on their own.

1. The Problem
Since the birth of Bitcoin, all cryptocurrencies have failed to solve two fundamental problems:
The monopoly of capital over currency issuance rights: Under the PoW mechanism, capital can monopolize bookkeeping and issuance rights by purchasing computing power; under the PoS mechanism, capital can monopolize staking rights and issuance rights by holding tokens; all other consensus mechanisms ultimately evolve into a game of capital.
Exploitation caused by information asymmetry: The circulation history and flow of funds are obscured, allowing money laundering, fraud, and speculative activities to thrive.
The root of the problem lies in the fact that all such currencies attempt to seek fairness in the spatial dimension and all retain artificially designed information barriers.
The only resource that cannot be bought by capital, cannot be accelerated, and cannot be forged, is time.
The only method that can completely eliminate exploitation is complete, unconditional transparency.

2. Three Unshakable Core Rules
The entire set of rules for Time Coin consists only of the following three articles. There are no exceptions, no patches, and no hidden clauses.

Rule One: One Device, One Vote, One Wallet
Any single independent physical computing device possesses and can only possess one node identity and one bound wallet. This binding relationship, once established, cannot be dissolved. Each node can receive, and can only receive, one Time Coin per consensus cycle.
The node identity is automatically generated from the device's built-in Physical Unclonable Function (PUF) chip and the Bitcoin block height hash. It is globally unique and non-repeatable. Resetting the system will permanently lose the wallet, and only a new wallet can be regenerated.
The wallet private key is physically derived at the hardware layer by the PUF chip and never exists outside the chip in any digital form (such as mnemonic phrases or ciphertext). The user's control over the wallet is equivalent to absolute possession of the physical device; there is no "independent custody" separate from the device.
When a device's PUF fails due to aging, damage, or any other reason, that node dies permanently and stops generating Time Coin; any Time Coin already in its wallet will be permanently frozen along with that node and exit circulation. No one can transfer or recover them. If the device ages, existing Time Coin in the wallet can be transferred in advance to any other valid node. If the device is lost, the only recovery method is to retrieve the device.
Any operation such as resetting the system, formatting the device, or replacing the chip will permanently destroy the locally stored wallet private key and all Time Coin data.
Even on the same physical device, the node identity and wallet generated after a reset are entirely new and independent, bearing no relation to the previous identity and wallet.
All Time Coin in the original wallet, having permanently lost the ability to obtain signature authorization from the original PUF chip, can never again participate in any transaction, effectively equivalent to physical destruction. This is like throwing cash into a fire: the money itself has not vanished, but it can never be used by anyone again.
Pure software virtual environments (without a physical PUF chip) cannot generate valid node identities and wallets.
The node rights of all devices are completely equal: a $50 Raspberry Pi = a $10,000 phone = a $100 million supercomputer.
Any device, at any location, receives exactly the same yield per unit of time.

Timeline Lockdown:
The economic life of a physical device possesses absolute exclusivity. When a device's PUF chip is first activated by any compliant client based on this protocol, an irreversible "protocol lock" flag is generated inside the PUF's secure enclave.
Once locked, that PUF chip absolutely refuses, at the physical level, to perform handshake or signing computations with any other protocol fork client.
Within the lifecycle of a single physical device, it can, and inevitably must, participate in the time proof of only one Time Coin fork chain. If a node entity intends to participate in another fork chain, the only legal path is to acquire another brand new, unactivated physical device.
This protocol deprives a single physical device of the right to simultaneously hold multiple time-based currencies. The choice of which time rule to follow must be paid for with the corresponding physical hardware cost.

Rule Two: Time Standard · Full-Chain Transparency
The sole basis for Time Coin issuance is verifiable online computing time. The complete lifecycle of every single Time Coin will be permanently recorded in an immutable manner.
No pre-mining, no founder rewards, no institutional allocations, no form of advance distribution whatsoever.
There is no fixed total supply cap; the issuance volume is automatically proportional to the number of active nodes across the network.
There is no offline time compensation; only nodes that complete continuous VDF calculations online can receive Time Coin.
All nodes compute the same Verifiable Delay Function (VDF) simultaneously, based on the same Bitcoin block hash.
The non-parallelizable nature of the VDF ensures that the only difference in completion time among all nodes is due to physical variance.
All devices that finish computing early must wait for the network-wide broadcast of the next consensus cycle before continuing.
The consensus cycle is an integer multiple of the VDF computation count, determined by real-time weighted voting of all nodes.
For every consensus cycle of continuous VDF computation completed, all active nodes simultaneously receive one and only one Time Coin.
Every single Time Coin will permanently record the block height of its birth and the PUF identifier of its generating device.
Every transaction of every single Time Coin permanently records the transaction time and the wallet identifiers of both sender and receiver, achieving one independent ledger per Time Coin.
Ownership of Time Coin can only be transferred via peer-to-peer transfer; any form of export, duplication, or backup is invalid.
Every Time Coin inherently carries a complete transaction history chain; any transfer of ownership must add a new transaction record to the history chain of that Time Coin itself.
Every transaction must be validated by the PUF chip signature of the sending device before it can take effect.
Each Time Coin is the smallest unit, indivisible, and can only be transacted in integer multiples.
Any Time Coin data that leaves its corresponding wallet loses its complete history chain, cannot be verified by the entire network nodes, and is considered invalid currency.

Definition of Time Coin: Unit and Circulation
Smallest unit: 1 Time Coin
The Time Coin is an indivisible, uncuttable, non-subdividable complete unit of value, corresponding to the unique time output of a single device within one consensus cycle.

Non-Mergeable Time Coin Ontology
Any multiple Time Coins cannot be merged, combined, or compressed. Every single Time Coin, from its birth to the cessation of its circulation, perpetually maintains an independent identity and independent history chain.

Integer Transactions Only
All transfers, payments, and exchanges can only be conducted in integer amounts of 1, 2, 3... No decimals, no change splitting.

History Only Appends, Never Alters
The transaction history of each Time Coin can only append new records; it cannot be deleted, tampered with, overwritten, merged, or simplified.

Departure from Wallet Means Death
The sole legitimate environment for a Time Coin's existence is the hardware secure enclave within the "hot wallet" memory area protected by the device's PUF chip hardware-level encryption.

Export Prohibition: Time Coin data and its derived private keys are absolutely forbidden to leave the PUF secure enclave in any form (export files, screenshots, copy-paste, plaintext network transmission) and enter conventional operating system memory or external storage. Once such a downgrade occurs, it immediately triggers a "history break," and its internal state is instantly marked by the system as "history broken."

Re-import Prohibition: Any behavior attempting to re-import Time Coin data that has ever left the PUF environment back into a wallet will be automatically recognized and rejected by the entire network nodes.

Fragmentation Equals Invalid Coin: When a transaction is initiated, the receiving party's PUF, upon receiving the data, will verify the causal chain of that Time Coin. If it discovers any spliced traces within the chain not generated by a PUF physical signature, or detects conditions such as timestamp inversion or hash breaks, it is judged as "history fragmentation." A Time Coin that triggers an alert is rejected by the entire network and considered invalid currency.

Legitimate Peer-to-Peer Enclave Handshake: The only permitted "transfer" is a "state-append handshake" conducted directly between the PUF secure enclaves of two online devices via an encrypted channel. The Time Coin data packet must never pass through any third-party server or non-PUF environment under any circumstances.

Transactions Are State Append, Not Data Relocation
When a user replaces an old phone with a new one, the experience feels like "Time Coin has been transferred to the new phone," but in the underlying logic:
The old phone's PUF secure enclave physically signs and appends a record to the end of the local Time Coin's causal chain: "Control transferred to new phone PUF hash."
Subsequently, the old PUF enclave establishes a peer-to-peer encrypted tunnel with the new PUF enclave and directly pushes this "complete Time Coin data with its updated tail" into the new phone's PUF enclave. Throughout the entire process, the Time Coin data never touches any conventional operating system, achieving absolute security isolation.

The Sole Purpose of the Blockchain: Time Notarization
The underlying network of this protocol (such as the Bitcoin blockchain) does not assume a "bookkeeping" function; it merely serves as an "absolute time notary."
Whenever a Time Coin internally appends a transfer record, the existence of the blockchain is solely to provide an "immutable external timestamp hash" for the internal causal chain of the Time Coin, used to assist in proving that its history has not been rolled back. The blockchain does not store any transaction data or user information of Time Coin.

Rule Three: Universal Real-Time Governance
The sole mechanism for adjusting any system parameter is the continuous real-time weighted voting of all active nodes. The consequences of any adjustment are borne jointly by all nodes.
The only adjustable parameter is the length of the consensus cycle.
The system presets 15 options for exponentially growing consensus cycles. Any node can choose any option at any time and can change its choice at any time.
Votes, as part of the node's state, propagate automatically across the entire network with the node's heartbeat.
All nodes independently calculate and verify the network-wide voting result, taking the vote shares of the top 10 options with the highest total votes to calculate a weighted average, thereby deriving the current effective consensus cycle.
The effective consensus cycle is automatically updated and takes effect immediately every 10 minutes. There are no voting periods, no approval processes, and no central statistical node.
Credentials generated without accepting the consensus, or by tampering with the time cycle, do not possess Time Coin properties within this time chain, are considered invalid data, and will be directly rejected for reception, verification, and transaction by all network nodes.
Consensus can be formed with two or more devices online.
Adjustment of any other parameter is illegal.

3. Self-Regulating Mechanism
Time Coin requires no human intervention; it is a perfectly self-balancing system.

Automatic Dissolution of Capital Attacks
If a capital party purchases a large number of devices attempting to monopolize issuance rights, the following multi-layered automatic balancing mechanisms will be triggered:
Increase in total network node count → Time Coin issuance volume increases synchronously → The price of a single Time Coin automatically falls.
All nodes vote to extend the consensus cycle → The yield per unit time for all nodes decreases correspondingly.
The capital party's rigid costs for electricity, bandwidth, venue, and labor remain unchanged → Profits shrink dramatically.
Large-scale mining farms will face exponentially increasing manual transaction costs; the larger the scale, the more severe the loss.
When revenue falls below cost, the capital party automatically shuts down and leaves → The system returns to equilibrium.
Individual users are almost entirely unaffected (smart devices are already in long-term operation, and the marginal cost of participating as a node is nearly zero).

Automatic Price Stability
The value of Time Coin is perpetually anchored to the benchmark of "1 Time Coin = verifiable human time of 1 consensus cycle." Its price will not stabilize around the operating cost; instead, the operating cost will automatically stabilize around the price of Time Coin.
Time Coin price rises → More users run nodes → Supply increases → Price falls back.
Time Coin price falls → Speculators leave → Supply decreases → Price rebounds.
This mechanism inherently avoids dramatic surges, crashes, and speculative hype. The price of Time Coin is essentially the fair price of time.

Automatic Isolation of Toxic Assets
All transaction histories are completely open and transparent; the market will automatically complete screening and isolation:
Time Coins involved in illegal transactions will be spontaneously refused acceptance by most merchants and users.
Any market entity can autonomously refuse any Time Coin involved in illegal transactions, without needing approval from any third party.
There is no unified, mandatory blacklist; all filtering behavior is voluntary and market-driven.

4. Security
The security of Time Coin is jointly guaranteed by physics and mathematics:
Sybil Attack Immunity: The combination of PUF and Bitcoin block height hash ensures that a single physical device can only generate one unique node identity over its entire lifecycle.
Computational Power Attack Immunity: VDF is non-parallelizable; the level of computing power does not affect the yield per unit time.
Theft Immunity: The wallet private key is completely controlled by the user; the system stores no private keys.
Double-Spend Immunity: Time Coin can only be transferred peer-to-peer between compliant wallets and cannot exist independently separate from its corresponding wallet.
51% Computational Power Attack Immunity: Acquiring 51% of issuance rights would require controlling 51% of the world's smart devices, which is economically unfeasible.

5. Forks and Evolution
This protocol does not prohibit forks. Any fork based on this protocol is legal, and users are free to choose any chain to use.

Forks are the system's self-evolution mechanism. If a fork modifies the rules of this protocol and gains recognition from more users, it will become the de facto main chain. All forks not recognized by users will naturally perish due to the absence of active nodes running them.
No individual or organization has the right to determine which chain is "official." The sole arbiter is the free choice of all users.

A single device can only compute one VDF at any given time. Therefore, if one device installs two or more time fork wallets simultaneously, due to the non-parallelizability of computation, the redundant wallets will be unable to produce valid time proofs, and will be directly judged as invalid at the protocol level.

Absolute Isolation of the Time Dimension: The time scales of various fork chains are mutually independent; a Time Coin only possesses circulation legitimacy within the time chain where it was born. Any cross-chain transfer behavior cannot generate a continuous PUF signature causal chain at the cryptographic level, effectively equivalent to physical destruction and re-generation. The possibility of cross-chain circulation does not exist.

All Time Coins based on this protocol and their forks must be completely open-source to allow verification of the authenticity and compliance of their protocol implementation.

6. The Philosophical Declaration of Time Coin
Absolute Decentralization: The Total Dissolution of Power and the Birth of a Self-Evident System
Time Coin does not pursue decentralization, because within the underlying architecture of Time Coin, the concept of a "center" simply does not exist. All past monetary systems, regardless of their technological packaging, have never been able to escape three implicit supreme powers: issuance rights, bookkeeping rights, and rule adjudication rights. Through the rigid constraints of physics and mathematics, Time Coin completely "dissolves" these three powers, returning them to every independent individual node.

1. The Dissolution of Issuance Rights: From "Third-Party Granting" to "Self-Evident Time"
Within the Time Coin network, no entity possesses the privilege of issuing currency. The act of "issuance" itself is downgraded to the objective physical phenomenon of "time elapsing while a physical device is online."
No miner block rewards needed, no staking for interest. Your device exists, time passes, the VDF computation is completed, and the coin is "natively" generated inside your device. Time Coin has no issuer, only witnesses of time.

2. The Dissolution of Bookkeeping Rights: From "Global Dependency" to "One Coin, One Proof"
Traditional blockchains rely on all network nodes to jointly maintain a single "general ledger," meaning the legitimacy of your assets must depend on the acknowledgment of strangers.
Time Coin's "one coin, one ledger" mechanism completely severs the dependency on a global ledger. Every Time Coin inherently carries an immutable causal chain; its legitimacy does not depend on records from any external node, but solely on the continuity of its own history and the PUF physical signatures of every controller in its chain. Others can neither help you keep your books nor tamper with your ledger.

3. The Dissolution of Rule Adjudication Rights: From "Code Dictatorship" to "Real-Time Emergence"
In the Time Coin protocol, the adjustment power for the sole variable parameter (the length of the consensus cycle) does not reside in the hands of any developer, foundation, or super-node. It is entirely derived in real-time through weighted voting by all active nodes during every heartbeat cycle.
There are no proposals, no voting days, no community governance committees. The system's rules adaptively emerge in real-time based on the current number of nodes, much like the flow rate of water. Time Coin has no ruler, only the physical-level self-consistency of algorithms.

7. Conclusion
Time Coin is not a replacement for Bitcoin, but the completion of Bitcoin.
Bitcoin achieved "the inviolability of existing stock."
Time Coin achieves "the fair sharing of incremental value" and "full-chain transparency."
Time Coin does not attempt to replace fiat currency, nor to eliminate nations, but awaits the arrival of a human community. It does not command anyone to do anything, nor does it prohibit anyone from doing anything. It merely provides the most basic framework, and then lets all of humanity engage in their own negotiations, self-regulate, and create the future themselves.
Time Coin has not created any new rules; it has simply written the universe's most fundamental laws—"the passage of time, the irreversibility of causality"—into code.

This is "Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei."

This is Tian zhi dao.

This white paper is the sole official normative document for the Time Coin protocol. This protocol has no official code, no official implementation, no official website, no founder, and no form of official organization. Any entity is free to implement this protocol. All protocol implementations that conform to the rules of this white paper are valid Time Coin protocols.
Because true justice needs no father.

Signed: Dao Heng Wu Ming

------------------------------------------------------------------------

[Français]

Résumé
Ce document propose le tout premier système monétaire décentralisé purement fondé sur le temps dans l'histoire de l'humanité. Ce système repose sur les fonctions physiques non clonables (PUF) pour réaliser le mécanisme central « un appareil, une voix, un portefeuille », sur les fonctions de délai vérifiable (VDF) pour garantir l'infalsifiabilité du temps, et sur la blockchain Bitcoin pour assurer la sécurité ultime et la transparence intégrale de la chaîne.
L'unique base d'émission du Time Coin est le temps en ligne vérifiable. Toute entité possédant un appareil intelligent connectable, en consacrant un temps vérifiable équivalent, reçoit une quantité équivalente de Time Coins. Il n'y a aucun seuil de capital, aucun seuil technique, aucun seuil d'identité. Le seul moyen de modifier un quelconque paramètre du système est le vote en temps réel de tous les nœuds, selon le principe une personne, une voix.
Le Time Coin ne tente pas de concevoir l'équité ; il est l'équité elle-même. Il ne tente pas de dissimuler la moindre information ; il est lui-même la transparence totale. Il ne tente pas de résoudre les problèmes ; il laisse les problèmes se dissoudre d'eux-mêmes.

1. Le problème
Depuis la naissance de Bitcoin, toutes les cryptomonnaies ont échoué à résoudre deux problèmes fondamentaux :
Le monopole du capital sur le droit d'émission monétaire : dans le mécanisme PoW, le capital peut monopoliser le droit de tenue de registre et d'émission en achetant de la puissance de calcul ; dans le mécanisme PoS, le capital peut monopoliser le droit de participation et d'émission en détenant des jetons ; tous les autres mécanismes de consensus finissent par se muer en un jeu de capital.
L'exploitation causée par l'asymétrie d'information : l'historique de circulation et les flux de fonds sont occultés, ce qui permet au blanchiment d'argent, à la fraude et aux activités spéculatives de prospérer.
La racine du problème réside dans le fait que toutes ces monnaies tentent de chercher l'équité dans la dimension spatiale, tout en conservant des barrières informationnelles artificiellement conçues.
La seule ressource qui ne peut être achetée par le capital, qui ne peut être accélérée et qui ne peut être falsifiée, c'est le temps.
La seule méthode capable d'éliminer totalement l'exploitation est la transparence complète et inconditionnelle.

2. Trois règles fondamentales et inébranlables
L'intégralité des règles du Time Coin se compose uniquement des trois articles suivants. Il n'existe aucune exception, aucun correctif et aucune clause cachée.

Règle un : Un appareil, une voix, un portefeuille
Tout appareil informatique physique indépendant possède, et ne peut posséder, qu'une seule identité de nœud et un seul portefeuille lié. Cette relation de liaison, une fois établie, ne peut être dissoute. Chaque nœud peut recevoir, et ne peut recevoir, qu'un seul Time Coin par cycle de consensus.
L'identité du nœud est générée automatiquement à partir de la puce PUF intégrée à l'appareil et du hash de la hauteur de bloc Bitcoin. Elle est unique au monde et non reproductible. La réinitialisation du système entraîne la perte définitive du portefeuille ; seul un nouveau portefeuille peut alors être généré.
La clé privée du portefeuille est dérivée physiquement dans la couche matérielle par la puce PUF et n'existe jamais en dehors de la puce sous une forme numérique quelconque (comme une phrase mnémonique ou un texte chiffré). Le contrôle du portefeuille par l'utilisateur équivaut à la possession absolue de l'appareil physique ; il n'existe pas de « conservation indépendante » séparée de l'appareil.
Lorsque la PUF d'un appareil devient défaillante en raison du vieillissement, de dommages ou de toute autre cause, ce nœud meurt définitivement et cesse de générer des Time Coins ; les Time Coins déjà présents dans son portefeuille seront gelés de manière permanente avec ce nœud et sortiront de la circulation. Nul ne peut les transférer ni les récupérer. En cas de vieillissement de l'appareil, les Time Coins existants dans le portefeuille peuvent être transférés à l'avance vers n'importe quel autre nœud valide. En cas de perte de l'appareil, la seule méthode de récupération est de retrouver l'appareil.
Toute opération telle que la réinitialisation du système, le formatage de l'appareil ou le remplacement de la puce détruira de manière permanente la clé privée du portefeuille stockée localement ainsi que toutes les données des Time Coins.
Même sur le même appareil physique, l'identité de nœud et le portefeuille générés après une réinitialisation sont entièrement nouveaux et indépendants, sans aucun lien avec l'identité et le portefeuille précédents.
Tous les Time Coins du portefeuille d'origine, ayant définitivement perdu la possibilité d'obtenir l'autorisation de signature de la puce PUF d'origine, ne pourront plus jamais participer à aucune transaction, ce qui équivaut à une destruction physique. C'est comme jeter de l'argent liquide dans le feu : l'argent lui-même n'a pas disparu, mais il ne pourra plus jamais être utilisé par quiconque.
Les environnements virtuels purement logiciels (sans puce PUF physique) ne peuvent pas générer d'identité de nœud ni de portefeuille valides.
Les droits de nœud de tous les appareils sont totalement égaux : un Raspberry Pi à 50 $ = un téléphone à 10 000 $ = un supercalculateur à 100 millions $.
N'importe quel appareil, en n'importe quel lieu, reçoit exactement le même rendement par unité de temps.

Verrouillage de la ligne temporelle :
La vie économique d'un appareil physique possède une exclusivité absolue. Lorsque la puce PUF d'un appareil est activée pour la première fois par un client conforme basé sur ce protocole, un drapeau irréversible de « verrou de protocole » est généré à l'intérieur de l'enclave sécurisée de la PUF.
Une fois verrouillée, cette puce PUF refuse absolument, au niveau physique, d'effectuer toute poignée de main ou tout calcul de signature avec tout autre client d'une bifurcation du protocole.
Au cours du cycle de vie d'un même appareil physique, il ne peut, et ne pourra inévitablement, participer qu'à la preuve de temps d'une seule chaîne de bifurcation du Time Coin. Si une entité nœud souhaite participer à une autre chaîne de bifurcation, la seule voie légale est d'acquérir un autre appareil physique entièrement neuf et non activé.
Ce protocole prive un appareil physique unique du droit de détenir simultanément plusieurs monnaies fondées sur le temps. Le choix de la règle temporelle doit être payé par le coût matériel physique correspondant.

Règle deux : Étalon-temps · Transparence intégrale de la chaîne
L'unique base d'émission du Time Coin est le temps de calcul en ligne vérifiable. Le cycle de vie complet de chaque Time Coin sera enregistré de manière permanente et immuable.
Pas de pré-minage, pas de récompense pour les fondateurs, pas de part institutionnelle, aucune forme de distribution anticipée.
Il n'y a pas de plafond d'offre totale fixe ; le volume d'émission est automatiquement proportionnel au nombre de nœuds actifs sur l'ensemble du réseau.
Il n'y a pas de compensation pour le temps hors ligne ; seuls les nœuds qui accomplissent des calculs VDF continus en ligne peuvent recevoir des Time Coins.
Tous les nœuds calculent simultanément la même fonction de délai vérifiable (VDF) sur la base du même hash de bloc Bitcoin.
La nature non parallélisable de la VDF garantit que la seule différence dans le temps d'achèvement entre tous les nœuds est due à la variance physique.
Tous les appareils qui terminent le calcul plus tôt doivent attendre la diffusion réseau du prochain cycle de consensus pour continuer.
Le cycle de consensus est un multiple entier du nombre de calculs VDF, déterminé par un vote pondéré en temps réel de tous les nœuds.
À chaque cycle de consensus de calcul VDF continu accompli, tous les nœuds actifs reçoivent simultanément un et un seul Time Coin.
Chaque Time Coin enregistrera de manière permanente la hauteur de bloc de sa naissance et l'identifiant PUF de l'appareil générateur.
Chaque transaction de chaque Time Coin enregistre de façon permanente l'heure de la transaction et les identifiants de portefeuille de l'expéditeur et du destinataire, réalisant ainsi un registre indépendant par Time Coin.
La propriété du Time Coin ne peut être transférée que par transfert pair-à-pair ; toute forme d'exportation, de duplication ou de sauvegarde est invalide.
Chaque Time Coin porte intrinsèquement une chaîne d'historique de transactions complète ; tout transfert de propriété doit ajouter un nouvel enregistrement de transaction à la chaîne d'historique de ce Time Coin même.
Chaque transaction doit être validée par la signature de la puce PUF de l'appareil émetteur avant de pouvoir prendre effet.
Chaque Time Coin est l'unité minimale, indivisible, et ne peut être échangé qu'en multiples entiers.
Toute donnée de Time Coin qui quitte son portefeuille correspondant perd sa chaîne d'historique complète, ne peut être vérifiée par les nœuds du réseau entier et est considérée comme une monnaie invalide.

Définition du Time Coin : Unité et circulation
Unité minimale : 1 Time Coin
Le Time Coin est une unité de valeur complète, indivisible, insécable et non subdivisible, correspondant à la production temporelle unique d'un seul appareil durant un cycle de consensus.

Ontologie non fusionnable du Time Coin
Aucun multiple de Time Coins ne peut être fusionné, combiné ou compressé. Chaque Time Coin, de sa naissance jusqu'à la fin de sa circulation, conserve perpétuellement une identité indépendante et une chaîne d'historique indépendante.

Transactions en nombres entiers uniquement
Tous les transferts, paiements et échanges ne peuvent être effectués qu'en nombres entiers : 1, 2, 3… Pas de décimales, pas de division pour rendre la monnaie.

Historique uniquement extensible, jamais modifiable
L'historique des transactions de chaque Time Coin ne peut que recevoir de nouveaux enregistrements ; il ne peut être supprimé, altéré, écrasé, fusionné ou simplifié.

Quitter le portefeuille signifie la mort
Le seul environnement légitime pour l'existence d'un Time Coin est l'enclave matérielle sécurisée au sein de la zone mémoire du « portefeuille chaud », protégée par le chiffrement de niveau matériel de la puce PUF de l'appareil.

Interdiction d'exportation : Les données du Time Coin et leurs clés privées dérivées sont absolument interdites de quitter l'enclave sécurisée PUF sous quelque forme que ce soit (fichier d'exportation, capture d'écran, copier-coller, transmission en clair sur le réseau) pour entrer dans la mémoire du système d'exploitation conventionnel ou un stockage externe. Dès qu'une telle rétrogradation se produit, elle déclenche immédiatement une « rupture d'historique », et son état interne est instantanément marqué par le système comme « historique rompu ».

Interdiction de réimportation : Toute tentative de réimporter dans un portefeuille des données de Time Coin ayant un jour quitté l'environnement PUF sera automatiquement reconnue et rejetée par tous les nœuds du réseau.

La fragmentation équivaut à une monnaie invalide : Lorsqu'une transaction est initiée, la PUF du destinataire, à la réception des données, vérifie la chaîne causale de ce Time Coin. Si elle découvre des traces d'assemblage dans la chaîne qui n'ont pas été générées par une signature physique PUF, ou si elle détecte des conditions telles qu'une inversion d'horodatage ou une rupture de hachage, cela est jugé comme une « fragmentation d'historique ». Un Time Coin qui déclenche une alerte est rejeté par l'ensemble du réseau et considéré comme une monnaie invalide.

Poignée de main légitime d'enclave à enclave en pair-à-pair : Le seul « transfert » autorisé est une « poignée de main d'ajout d'état » effectuée directement entre les enclaves sécurisées PUF de deux appareils en ligne via un canal chiffré. Le paquet de données du Time Coin ne doit en aucun cas transiter par un serveur tiers ou un environnement non PUF.

Les transactions sont un ajout d'état, pas un déplacement de données
Lorsqu'un utilisateur remplace un ancien téléphone par un nouveau, l'expérience donne l'impression que « les Time Coins ont été transférés vers le nouveau téléphone », mais dans la logique sous-jacente :
L'enclave sécurisée PUF de l'ancien téléphone signe physiquement et ajoute un enregistrement à la fin de la chaîne causale du Time Coin local : « Contrôle transféré au hash PUF du nouveau téléphone ».
Ensuite, l'ancienne enclave PUF établit un tunnel chiffré pair-à-pair avec la nouvelle enclave PUF et pousse directement cette « donnée complète du Time Coin avec sa queue mise à jour » dans l'enclave PUF du nouveau téléphone. Durant tout le processus, les données du Time Coin ne touchent jamais aucun système d'exploitation conventionnel, réalisant ainsi une isolation de sécurité absolue.

La seule fonction de la blockchain : notarisation temporelle
Le réseau sous-jacent de ce protocole (comme la blockchain Bitcoin) n'assume pas de fonction de « tenue de registre » ; il joue uniquement le rôle de « notaire temporel absolu ».
Chaque fois qu'un Time Coin ajoute en interne un enregistrement de transfert, l'existence de la blockchain sert uniquement à fournir un « hash d'horodatage externe immuable » pour la chaîne causale interne du Time Coin, afin d'aider à prouver que son historique n'a pas été annulé. La blockchain ne stocke aucune donnée de transaction ni aucune information d'utilisateur des Time Coins.

Règle trois : Gouvernance universelle en temps réel
Le seul mécanisme d'ajustement de tout paramètre du système est le vote pondéré continu en temps réel de tous les nœuds actifs. Les conséquences de tout ajustement sont supportées conjointement par tous les nœuds.
Le seul paramètre ajustable est la durée du cycle de consensus.
Le système prédéfinit 15 options pour des cycles de consensus à croissance exponentielle. N'importe quel nœud peut choisir n'importe quelle option à tout moment et peut modifier son choix à tout moment.
Les votes, en tant que partie de l'état du nœud, se propagent automatiquement sur l'ensemble du réseau avec le battement de cœur du nœud.
Tous les nœuds calculent et vérifient indépendamment le résultat du vote à l'échelle du réseau, en prenant les parts de vote des 10 options ayant obtenu le plus grand nombre total de votes pour calculer une moyenne pondérée, déterminant ainsi le cycle de consensus effectif actuel.
Le cycle de consensus effectif est automatiquement mis à jour et prend effet immédiatement toutes les 10 minutes. Il n'y a pas de période de vote, pas de processus d'approbation et pas de nœud central de statistiques.
Les preuves générées sans accepter le consensus, ou en falsifiant le cycle temporel, ne possèdent pas les propriétés du Time Coin au sein de cette chaîne temporelle, sont considérées comme des données invalides, et seront directement rejetées pour réception, vérification et transaction par tous les nœuds du réseau.
Un consensus peut être formé à partir de deux appareils en ligne ou plus.
L'ajustement de tout autre paramètre est illégal.

3. Mécanisme d'autorégulation
Le Time Coin n'exige aucune intervention humaine ; c'est un système parfaitement auto-équilibrant.

Dissolution automatique des attaques capitalistiques
Si une entité capitaliste achète un grand nombre d'appareils pour tenter de monopoliser le droit d'émission, les mécanismes d'équilibrage automatique à plusieurs niveaux suivants se déclencheront :
Augmentation du nombre total de nœuds du réseau → le volume d'émission de Time Coins augmente de manière synchrone → le prix d'un Time Coin baisse automatiquement.
Tous les nœuds votent pour allonger le cycle de consensus → le rendement par unité de temps de tous les nœuds diminue en proportion.
Les coûts rigides de l'entité capitaliste pour l'électricité, la bande passante, le site et la main-d'œuvre restent inchangés → les profits chutent drastiquement.
Les fermes de minage à grande échelle seront confrontées à des coûts de transaction manuelle en croissance exponentielle ; plus l'échelle est grande, plus les pertes sont sévères.
Lorsque les revenus tombent en dessous des coûts, l'entité capitaliste s'éteint automatiquement et quitte le réseau → le système retourne à l'équilibre.
Les utilisateurs individuels ne sont pratiquement pas affectés (les appareils intelligents fonctionnent déjà en continu, et le coût marginal de participation en tant que nœud est quasi nul).

Stabilité automatique des prix
La valeur du Time Coin est perpétuellement ancrée au repère « 1 Time Coin = le temps humain vérifiable d'un cycle de consensus ». Son prix ne se stabilisera pas autour du coût de fonctionnement ; au contraire, le coût de fonctionnement se stabilisera automatiquement autour du prix du Time Coin.
Le prix du Time Coin monte → plus d'utilisateurs font fonctionner des nœuds → l'offre augmente → le prix redescend.
Le prix du Time Coin baisse → les spéculateurs partent → l'offre diminue → le prix remonte.
Ce mécanisme évite intrinsèquement les envolées, les effondrements et la spéculation. Le prix du Time Coin est par essence le juste prix du temps.

Isolement automatique des actifs toxiques
Tous les historiques de transactions sont totalement ouverts et transparents ; le marché réalisera automatiquement le filtrage et l'isolement :
Les Time Coins ayant participé à des transactions illégales se verront spontanément refuser leur acceptation par la plupart des commerçants et utilisateurs.
Toute entité de marché peut refuser de manière autonome n'importe quel Time Coin impliqué dans une transaction illégale, sans avoir besoin de l'approbation d'un tiers.
Il n'existe pas de liste noire unifiée et obligatoire ; tous les comportements de filtrage sont volontaires et pilotés par le marché.

4. Sécurité
La sécurité du Time Coin est garantie conjointement par la physique et les mathématiques :
Immunité contre les attaques Sybil : La combinaison de la PUF et du hash de la hauteur de bloc Bitcoin garantit qu'un seul appareil physique ne peut générer qu'une seule identité de nœud unique sur tout son cycle de vie.
Immunité contre les attaques par puissance de calcul : La VDF est non parallélisable ; le niveau de puissance de calcul n'affecte pas le rendement par unité de temps.
Immunité contre le vol : La clé privée du portefeuille est entièrement contrôlée par l'utilisateur ; le système ne stocke aucune clé privée.
Immunité contre la double dépense : Le Time Coin ne peut être transféré qu'en pair-à-pair entre portefeuilles conformes et ne peut pas exister de manière indépendante séparé de son portefeuille correspondant.
Immunité contre l'attaque des 51 % de puissance de calcul : Acquérir 51 % des droits d'émission nécessiterait de contrôler 51 % des appareils intelligents de la planète, ce qui est économiquement irréalisable.

5. Bifurcations et évolution
Ce protocole n'interdit pas les bifurcations. Toute bifurcation basée sur ce protocole est légale, et les utilisateurs sont libres de choisir la chaîne qu'ils souhaitent utiliser.

Les bifurcations sont le mécanisme d'auto-évolution du système. Si une bifurcation modifie les règles de ce protocole et obtient la reconnaissance d'un plus grand nombre d'utilisateurs, elle deviendra la chaîne principale de facto. Toutes les bifurcations non reconnues par les utilisateurs périront naturellement en l'absence de nœuds actifs les exécutant.
Aucun individu ni aucune organisation n'a le droit de déterminer quelle chaîne est « officielle ». Le seul arbitre est le libre choix de l'ensemble des utilisateurs.

Un même appareil ne peut calculer qu'une seule VDF à un instant donné. Par conséquent, si un appareil installe simultanément deux portefeuilles de bifurcation temporelle ou plus, en raison de la non-parallélisabilité du calcul, les portefeuilles surnuméraires seront incapables de produire des preuves de temps valides, et seront directement jugés invalides au niveau du protocole.

Isolement absolu de la dimension temporelle : Les échelles de temps des différentes chaînes de bifurcation sont mutuellement indépendantes ; un Time Coin ne possède de légitimité de circulation qu'au sein de la chaîne temporelle où il est né. Tout comportement de transfert inter-chaînes ne peut pas générer une chaîne causale continue de signatures PUF au niveau cryptographique, ce qui équivaut effectivement à une destruction physique et à une régénération. La possibilité d'une circulation inter-chaînes n'existe pas.

Tous les Time Coins basés sur ce protocole et leurs bifurcations doivent être entièrement open source afin de permettre la vérification de l'authenticité et de la conformité de leur implémentation du protocole.

6. La déclaration philosophique du Time Coin
Décentralisation absolue : La dissolution totale du pouvoir et la naissance d'un système auto-évident
Le Time Coin ne poursuit pas la décentralisation, car dans l'architecture sous-jacente du Time Coin, le concept de « centre » n'existe tout simplement pas. Tous les systèmes monétaires passés, quelle que soit leur enveloppe technologique, n'ont jamais pu échapper à trois pouvoirs suprêmes implicites : le droit d'émission, le droit de tenue de registre et le droit de décision sur les règles. Grâce aux contraintes rigides de la physique et des mathématiques, le Time Coin « dissout » complètement ces trois pouvoirs, les restituant à chaque nœud individuel indépendant.

1. La dissolution du droit d'émission : de « l'octroi par un tiers » à « l'auto-preuve par le temps »
Au sein du réseau Time Coin, aucune entité ne possède le privilège d'émettre de la monnaie. L'acte d'« émission » lui-même est rétrogradé au rang de phénomène physique objectif de « temps qui s'écoule pendant qu'un appareil physique est en ligne ».
Pas besoin de récompense de bloc pour les mineurs, pas besoin de jalonnement pour générer des intérêts. Votre appareil existe, le temps passe, le calcul VDF s'achève, et la pièce est « nativement » générée à l'intérieur de votre appareil. Le Time Coin n'a pas d'émetteur, seulement des témoins du temps.

2. La dissolution du droit de tenue de registre : de la « dépendance globale » à « une pièce, une preuve »
Les blockchains traditionnelles reposent sur l'ensemble des nœuds du réseau pour maintenir conjointement un « grand livre général », ce qui signifie que la légitimité de vos actifs doit dépendre de la reconnaissance d'inconnus.
Le mécanisme « une pièce, un registre » du Time Coin rompt totalement la dépendance envers un registre global. Chaque Time Coin porte intrinsèquement une chaîne causale immuable ; sa légitimité ne dépend pas des enregistrements d'un nœud externe, mais uniquement de la continuité de son propre historique et des signatures physiques PUF de chacun de ses contrôleurs dans la chaîne. Les autres ne peuvent ni tenir vos comptes à votre place, ni falsifier votre registre.

3. La dissolution du droit de décision sur les règles : de la « dictature du code » à « l'émergence en temps réel »
Dans le protocole Time Coin, le pouvoir d'ajustement du seul paramètre variable (la durée du cycle de consensus) ne réside entre les mains d'aucun développeur, fondation ou super-nœud. Il est entièrement dérivé en temps réel par le vote pondéré de tous les nœuds actifs durant chaque cycle de battement de cœur.
Il n'y a pas de propositions, pas de jours de vote, pas de comités de gouvernance communautaire. Les règles du système émergent de manière adaptative en temps réel en fonction du nombre actuel de nœuds, à la manière du débit de l'eau. Le Time Coin n'a pas de dirigeant, seulement l'auto-cohérence de niveau physique des algorithmes.

7. Conclusion
Le Time Coin n'est pas un remplacement de Bitcoin, mais l'achèvement de Bitcoin.
Bitcoin a réalisé « l'inviolabilité du stock existant ».
Le Time Coin réalise « le partage équitable de l'accroissement » et « la transparence intégrale de la chaîne ».
Le Time Coin ne tente pas de remplacer la monnaie fiduciaire, ni d'éliminer les États, mais attend l'avènement d'une communauté humaine. Il n'ordonne à personne de faire quoi que ce soit, ni n'interdit à quiconque de faire quoi que ce soit. Il fournit simplement le cadre le plus élémentaire, puis laisse l'humanité tout entière engager ses propres négociations, s'autoréguler et créer elle-même l'avenir.
Le Time Coin n'a créé aucune règle nouvelle ; il a simplement inscrit dans le code les lois les plus fondamentales de l'univers : « le passage du temps, l'irréversibilité de la causalité ».

Ceci est « Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei ».

C'est le Tian zhi dao.

Ce livre blanc est l'unique document normatif officiel pour le protocole Time Coin. Ce protocole n'a pas de code officiel, pas d'implémentation officielle, pas de site web officiel, pas de fondateur et aucune forme d'organisation officielle. Toute entité est libre d'implémenter ce protocole. Toutes les implémentations du protocole qui sont conformes aux règles de ce livre blanc sont des protocoles Time Coin valides.
Car la justice véritable n'a pas besoin de père.

Signé : Dao Heng Wu Ming

------------------------------------------------------------------------

[Deutsch]

Zusammenfassung
Dieses Papier stellt das erste rein zeitbasierte dezentrale Währungssystem in der Menschheitsgeschichte vor. Das System implementiert den Kernmechanismus „ein Gerät, eine Stimme, eine Brieftasche“ auf Basis von Physical Unclonable Functions (PUF), erreicht die Unfälschbarkeit der Zeit durch Verifiable Delay Functions (VDF) und nutzt die Bitcoin-Blockchain für ultimative Sicherheit und vollständige Transparenz der gesamten Kette.
Die alleinige Ausgabegrundlage von Time Coin ist nachweisbare Online-Zeit. Jedes Subjekt, das ein vernetzbares intelligentes Gerät besitzt und eine gleiche Menge an nachweisbarer Zeit aufwendet, erhält eine gleiche Menge an Time Coins. Es gibt keine Kapitalhürde, keine technische Hürde, keine Identitätshürde. Die einzige Möglichkeit, irgendeinen Systemparameter anzupassen, ist die Echtzeit-Abstimmung aller Knoten nach dem Prinzip „eine Person, eine Stimme“.
Time Coin versucht nicht, Fairness zu gestalten; es ist die Fairness selbst. Es versucht nicht, irgendwelche Informationen zu verbergen; es ist selbst vollkommen transparent. Es versucht nicht, Probleme zu lösen; es lässt Probleme von selbst verschwinden.

1. Das Problem
Seit der Entstehung von Bitcoin haben alle Kryptowährungen zwei grundlegende Probleme nicht lösen können:
Das Kapitalmonopol über das Geldausgaberecht: Unter dem PoW-Mechanismus kann Kapital durch den Kauf von Rechenleistung das Buchführungs- und Ausgaberecht monopolisieren; unter dem PoS-Mechanismus kann Kapital durch das Halten von Token das Staking- und Ausgaberecht monopolisieren; alle übrigen Konsensmechanismen entwickeln sich letztlich zu einem Spiel des Kapitals.
Ausbeutung durch Informationsasymmetrie: Die Umlaufgeschichte und die Geldflüsse werden verschleiert, wodurch Schwarzgeld, Betrug und Spekulation gedeihen können.
Die Wurzel des Problems liegt darin, dass alle derartigen Währungen versuchen, Fairness in der räumlichen Dimension zu suchen, und alle künstlich gestaltete Informationsbarrieren beibehalten.
Die einzige Ressource, die nicht von Kapital gekauft, nicht beschleunigt und nicht gefälscht werden kann, ist Zeit.
Die einzige Methode, die Ausbeutung vollständig zu beseitigen, ist vollständige, bedingungslose Transparenz.

2. Drei unerschütterliche Kernregeln
Das gesamte Regelwerk von Time Coin besteht nur aus den folgenden drei Artikeln. Es gibt keine Ausnahmen, keine Patches und keine versteckten Klauseln.

Regel eins: Ein Gerät, eine Stimme, eine Brieftasche
Jedes unabhängige physische Rechengerät besitzt und kann nur eine Knotenidentität und eine gebundene Brieftasche besitzen; diese Bindung kann, einmal hergestellt, nicht gelöst werden. Jeder Knoten kann pro Konsenszyklus einen und nur einen Time Coin erhalten.
Die Knotenidentität wird automatisch aus der im Gerätechip eingebauten Physical Unclonable Function (PUF) und dem Hash der Bitcoin-Blockhöhe generiert. Sie ist weltweit einzigartig und nicht wiederholbar. Ein Zurücksetzen des Systems führt zum dauerhaften Verlust der Brieftasche; es kann nur eine neue Brieftasche generiert werden.
Der private Schlüssel der Brieftasche wird von dem PUF-Chip auf Hardwareebene physisch abgeleitet und existiert niemals außerhalb des Chips in irgendeiner digitalen Form (wie mnemonische Phrasen oder Chiffretext). Die Kontrolle des Nutzers über die Brieftasche entspricht dem absoluten Besitz des physischen Geräts; es gibt keine vom Gerät getrennte „unabhängige Verwahrung“.
Wenn die PUF eines Geräts aufgrund von Alterung, Beschädigung oder aus irgendeinem anderen Grund ausfällt, stirbt dieser Knoten dauerhaft und stellt die Generierung von Time Coins ein; die bereits in seiner Brieftasche vorhandenen Time Coins werden zusammen mit dem Knoten dauerhaft eingefroren, aus dem Umlauf genommen und können von niemandem transferiert oder wiederhergestellt werden. Bei Gerätealterung können vorhandene Time Coins in der Brieftasche vorab auf einen beliebigen anderen gültigen Knoten übertragen werden. Bei Geräteverlust ist die einzige Wiederherstellungsmethode, das Gerät wiederzufinden.
Jegliche Operation wie das Zurücksetzen des Systems, Formatieren des Geräts oder Austauschen des Chips zerstört dauerhaft den lokal gespeicherten privaten Schlüssel der Brieftasche und alle Time-Coin-Daten.
Selbst bei demselben physischen Gerät sind die nach einem Reset generierte Knotenidentität und Brieftasche völlig neu und unabhängig und haben keinerlei Verbindung zu der vorherigen Identität und Brieftasche.
Alle Time Coins in der ursprünglichen Brieftasche können, da sie die Signaturautorisierung des ursprünglichen PUF-Chips nicht mehr erhalten können, dauerhaft an keiner Transaktion mehr teilnehmen, was einer physischen Zerstörung gleichkommt. Das ist, als würde man Bargeld ins Feuer werfen: Das Geld selbst ist nicht verschwunden, kann aber nie wieder von jemandem verwendet werden.
Rein softwarebasierte virtuelle Umgebungen (ohne physischen PUF-Chip) können keine gültige Knotenidentität und Brieftasche generieren.
Die Knotenrechte aller Geräte sind völlig gleich: Ein Raspberry Pi für 50 Yuan = ein Handy für 10.000 Yuan = ein Supercomputer für 100 Millionen Dollar.
Jedes Gerät an jedem Ort erhält exakt denselben Ertrag pro Zeiteinheit.

Zeitlinien-Sperre:
Das wirtschaftliche Leben eines physischen Geräts besitzt absolute Exklusivität. Wenn der PUF-Chip eines Geräts zum ersten Mal von einem beliebigen, auf diesem Protokoll basierenden, konformen Client aktiviert wird, erzeugt die sichere Enklave im Inneren der PUF ein unumkehrbares „Protokollsperre“-Flag.
Einmal gesperrt, verweigert dieser PUF-Chip auf physischer Ebene absolut jeglichen Handshake oder jegliche Signaturberechnung mit einem anderen Protokoll-Fork-Client.
Innerhalb des Lebenszyklus eines einzelnen physischen Geräts kann es nur und notwendigerweise nur an dem Zeitbeweis einer einzigen Time-Coin-Fork-Chain teilnehmen. Beabsichtigt eine Knotenentität, an einer anderen Fork-Chain teilzunehmen, ist der einzige legale Weg, ein weiteres brandneues, nicht aktiviertes physisches Gerät zu erwerben.
Dieses Protokoll entzieht einem einzelnen physischen Gerät das Recht, mehrere zeitbasierte Währungen gleichzeitig zu besitzen. Die Wahl der Zeitregel muss mit den entsprechenden physischen Hardwarekosten bezahlt werden.

Regel zwei: Zeitstandard · Vollständige Kettentransparenz
Die alleinige Ausgabegrundlage von Time Coin ist nachweisbare Online-Rechenzeit. Der gesamte Lebenszyklus jedes einzelnen Time Coins wird unveränderlich und dauerhaft aufgezeichnet.
Kein Pre-Mining, keine Gründerbelohnungen, keine institutionellen Anteile, keinerlei Form von Vorabverteilung.
Es gibt keine feste Obergrenze für das Gesamtangebot; das Ausgabevolumen ist automatisch proportional zur Anzahl der aktiven Knoten im gesamten Netzwerk.
Es gibt keine Kompensation für Offline-Zeit; nur Knoten, die kontinuierliche VDF-Berechnungen online abschließen, können Time Coins erhalten.
Alle Knoten berechnen gleichzeitig dieselbe Verifiable Delay Function (VDF) auf Basis desselben Bitcoin-Block-Hashes.
Die Nichtparallelisierbarkeit der VDF stellt sicher, dass der einzige Unterschied in der Berechnungszeit zwischen allen Knoten auf physischer Varianz beruht.
Alle Geräte, die die Berechnung vorzeitig abschließen, müssen auf die netzweite Aussendung des nächsten Konsenszyklus warten, um fortzufahren.
Der Konsenszyklus ist ein ganzzahliges Vielfaches der Anzahl der VDF-Berechnungen und wird durch gewichtete Echtzeit-Abstimmung aller Knoten bestimmt.
Für jeden abgeschlossenen Konsenszyklus kontinuierlicher VDF-Berechnung erhalten alle aktiven Knoten gleichzeitig einen und nur einen Time Coin.
Jeder einzelne Time Coin wird dauerhaft die Blockhöhe seiner Entstehung und die PUF-Kennung des erzeugenden Geräts aufzeichnen.
Jede Transaktion jedes Time Coins zeichnet dauerhaft die Transaktionszeit und die Brieftaschenkennungen von Sender und Empfänger auf, wodurch ein unabhängiges Hauptbuch pro Time Coin realisiert wird.
Das Eigentum an Time Coin kann nur durch Peer-to-Peer-Übertragung übertragen werden; jegliche Form von Export, Vervielfältigung oder Sicherung ist ungültig.
Jeder Time Coin trägt von Natur aus eine vollständige Transaktionshistorienkette; jede Eigentumsübertragung muss einen neuen Transaktionsdatensatz zur Historienkette des Time Coins selbst hinzufügen.
Jede Überweisung muss durch die Signatur des PUF-Chips des sendenden Geräts validiert werden, bevor sie wirksam wird.
Jeder Time Coin ist die kleinste Einheit, unteilbar, und kann nur in ganzzahligen Vielfachen gehandelt werden.
Jegliche Time-Coin-Daten, die ihre entsprechende Brieftasche verlassen, verlieren ihre vollständige Historienkette, können nicht von den Knoten des gesamten Netzwerks verifiziert werden und gelten als ungültige Währung.

Definition von Time Coin: Einheit und Umlauf
Kleinste Einheit: 1 Time Coin
Der Time Coin ist eine unteilbare, unzerschneidbare, nicht unterteilbare vollständige Werteinheit, die der einzigartigen Zeitleistung eines einzelnen Geräts innerhalb eines Konsenszyklus entspricht.

Nicht zusammenführbare Time-Coin-Ontologie
Mehrere Time Coins können nicht fusioniert, zusammengeführt oder komprimiert werden. Jeder Time Coin behält von seiner Entstehung bis zum endgültigen Ende seines Umlaufs stets eine unabhängige Identität und eine unabhängige Historienkette.

Nur ganzzahlige Transaktionen
Alle Überweisungen, Zahlungen und Tauschvorgänge können nur in ganzzahligen Mengen von 1, 2, 3... durchgeführt werden; keine Dezimalstellen, kein Wechselgeld durch Teilung.

Historie wird nur erweitert, nie verringert; nur fortgesetzt, nie geändert
Die Transaktionshistorie jedes Time Coins kann nur neue Einträge hinzufügen; sie kann nicht gelöscht, manipuliert, überschrieben, zusammengeführt oder vereinfacht werden.

Verlässt es die Brieftasche, bedeutet das den Tod
Die einzige legitime Umgebung für die Existenz eines Time Coins ist die hardwaregesicherte Enklave im Speicherbereich der „Hot Wallet“, geschützt durch die Verschlüsselung auf Hardwareebene des PUF-Chips des Geräts.

Exportverbot: Time-Coin-Daten und ihre abgeleiteten privaten Schlüssel sind absolut untersagt, in jeglicher Form (Exportdatei, Screenshot, Kopieren und Einfügen, Klartextübertragung im Netzwerk) die PUF-sichere Enklave zu verlassen und in den konventionellen Betriebssystemspeicher oder externen Speicher zu gelangen. Sobald eine solche Herabstufung eintritt, wird sofort ein „Historienbruch“ ausgelöst, und sein interner Zustand wird vom System unverzüglich als „Historienbruch“ markiert.

Rückflussverbot: Jeder Versuch, Time-Coin-Daten, die jemals die PUF-Umgebung verlassen haben, wieder in eine Brieftasche zu importieren, wird automatisch von den Knoten des gesamten Netzwerks erkannt und abgelehnt.

Fragmentierung bedeutet ungültige Währung: Wenn eine Transaktion initiiert wird, überprüft die PUF des Empfängers beim Empfang der Daten die Kausalkette dieses Time Coins. Wenn in der Kette Spuren von Zusammenfügungen gefunden werden, die nicht durch eine physische PUF-Signatur erzeugt wurden, oder wenn Situationen wie Zeitstempelumkehrungen oder Hash-Brüche vorliegen, wird dies als „Historienfragmentierung“ beurteilt. Ein Time Coin, der einen Alarm auslöst, wird vom gesamten Netzwerk abgelehnt und als ungültig betrachtet.

Legitimer Peer-to-Peer-Enklaven-Handshake: Der einzig erlaubte „Transfer“ ist ein „Status-Anfüge-Handshake“, der direkt zwischen den PUF-sicheren Enklaven zweier Online-Geräte über einen verschlüsselten Kanal durchgeführt wird. Das Time-Coin-Datenpaket darf unter keinen Umständen über einen Drittanbieter-Server oder eine Nicht-PUF-Umgebung laufen.

Transaktionen sind Status-Anfügung, nicht Datenverschiebung
Wenn ein Benutzer ein altes Handy durch ein neues ersetzt, fühlt es sich so an, als ob „die Time Coins auf das neue Handy übertragen wurden“, aber in der zugrunde liegenden Logik:
Die PUF-sichere Enklave des alten Handys signiert physisch und fügt am Ende der lokalen Time-Coin-Kausalkette einen Datensatz an: „Kontrolle an PUF-Hash des neuen Handys übergeben“.
Anschließend baut die alte PUF-Enklave einen verschlüsselten Peer-to-Peer-Tunnel mit der neuen PUF-Enklave auf und schiebt diese „vollständigen Time-Coin-Daten mit aktualisiertem Ende“ direkt in die PUF-Enklave des neuen Handys. Während des gesamten Prozesses berühren die Time-Coin-Daten kein einziges konventionelles Betriebssystem, wodurch absolute Sicherheitsisolation erreicht wird.

Die einzige Aufgabe der Blockchain: Zeitnotariatsfunktion
Das zugrunde liegende Netzwerk dieses Protokolls (wie die Bitcoin-Blockchain) übernimmt keine „Buchführungs“-Funktion; es spielt lediglich die Rolle eines „absoluten Zeitnotars“.
Jedes Mal, wenn ein Time Coin intern einen Übertragungsdatensatz anfügt, dient die Existenz der Blockchain lediglich dazu, der internen Kausalkette des Time Coins einen „unveränderlichen externen Zeitstempel-Hash“ bereitzustellen, um zu belegen, dass seine Historie nicht zurückgerollt wurde. Die Blockchain speichert keinerlei Transaktionsdaten oder Benutzerinformationen von Time Coins.

Regel drei: Universelle Echtzeit-Governance
Die einzige Möglichkeit, irgendeinen Systemparameter anzupassen, ist die kontinuierliche gewichtete Echtzeit-Abstimmung aller aktiven Knoten. Die Konsequenzen jeglicher Anpassung werden von allen Knoten gemeinsam getragen.
Der einzige anpassbare Parameter ist die Länge des Konsenszyklus.
Das System gibt 15 Optionen für exponentiell wachsende Konsenszyklen vor; jeder Knoten kann jederzeit eine beliebige Option wählen und seine Wahl auch jederzeit ändern.
Die Stimme, als Teil des Knotenstatus, verbreitet sich automatisch mit dem Herzschlag des Knotens im gesamten Netzwerk.
Alle Knoten berechnen und verifizieren unabhängig das netzweite Abstimmungsergebnis, nehmen die Stimmanteile der Top-10-Optionen mit den höchsten Gesamtstimmen und berechnen einen gewichteten Durchschnitt, um den aktuell gültigen Konsenszyklus zu ermitteln.
Der gültige Konsenszyklus wird alle 10 Minuten automatisch aktualisiert und tritt sofort in Kraft; es gibt keine Abstimmungsperiode, keinen Genehmigungsprozess und keinen zentralen Statistik-Knoten.
Berechtigungsnachweise, die ohne Akzeptanz des Konsenses oder durch eigenmächtige Manipulation des Zeitzyklus erzeugt werden, besitzen innerhalb dieser Zeitkette keine Time-Coin-Eigenschaften, werden als ungültige Daten betrachtet und von allen Knoten des Netzwerks direkt für Empfang, Verifizierung und Transaktion abgelehnt.
Konsens kann bereits ab zwei online befindlichen Geräten gebildet werden.
Die Anpassung jeglicher anderer Parameter ist illegal.

3. Selbstregulierungsmechanismus
Time Coin benötigt keinerlei menschliches Eingreifen; es ist ein perfekt selbstausgleichendes System.

Automatische Auflösung von Kapitalangriffen
Wenn eine Kapitalpartei eine große Anzahl von Geräten kauft, um das Ausgaberecht zu monopolisieren, werden die folgenden mehrschichtigen automatischen Ausgleichsmechanismen ausgelöst:
Zunahme der Gesamtnetzwerkknotenzahl → Time-Coin-Ausgabevolumen steigt synchron → Preis eines einzelnen Time Coins fällt automatisch.
Alle Knoten stimmen für eine Verlängerung des Konsenszyklus → Der Ertrag pro Zeiteinheit aller Knoten sinkt entsprechend.
Die starren Kosten der Kapitalpartei für Strom, Bandbreite, Räumlichkeiten, Personal usw. bleiben unverändert → Die Gewinne schrumpfen drastisch.
Groß angelegte Mining-Farmen werden mit exponentiell wachsenden manuellen Transaktionskosten konfrontiert; je größer der Maßstab, desto schwerer die Verluste.
Wenn die Erträge unter die Kosten fallen, schaltet die Kapitalpartei automatisch ab und verlässt das Netzwerk → Das System kehrt zum Gleichgewicht zurück.
Einzelne Nutzer sind nahezu überhaupt nicht betroffen (intelligente Geräte laufen ohnehin im Dauerbetrieb; die Grenzkosten der Teilnahme als Knoten sind nahezu null).

Automatische Preisstabilität
Der Wert von Time Coin ist stets am Maßstab „1 Time Coin = die nachweisbare menschliche Zeit eines Konsenszyklus“ verankert. Sein Preis wird sich nicht in der Nähe der Betriebskosten stabilisieren; im Gegenteil, die Betriebskosten werden sich automatisch in der Nähe des Time-Coin-Preises stabilisieren.
Time-Coin-Preis steigt → Mehr Nutzer betreiben Knoten → Angebot steigt → Preis fällt zurück.
Time-Coin-Preis fällt → Spekulanten verlassen das Netzwerk → Angebot sinkt → Preis steigt wieder.
Dadurch werden extreme Kursschwankungen und Spekulationsspielräume von vornherein vermieden; der Preis von Time Coin ist im Wesentlichen der faire Preis der Zeit.

Automatische Isolierung toxischer Vermögenswerte
Alle Transaktionshistorien sind vollständig offen und transparent; der Markt wird automatisch die Aussiebung und Isolierung vornehmen:
Time Coins, die an illegalen Transaktionen beteiligt waren, werden von den meisten Händlern und Nutzern spontan abgelehnt.
Jede Marktteilnehmer kann aus eigenem Ermessen jeden Time Coin ablehnen, der in eine illegale Transaktion verwickelt ist, ohne dass eine Genehmigung Dritter erforderlich ist.
Es gibt keine einheitliche, verpflichtende Schwarze Liste; alle Filtermaßnahmen sind freiwillig und marktgesteuert.

4. Sicherheit
Die Sicherheit von Time Coin wird gemeinsam durch Physik und Mathematik gewährleistet:
Immun gegen Sybil-Angriffe: Die Kombination aus PUF und Bitcoin-Blockhöhen-Hash stellt sicher, dass ein physisches Gerät während seines gesamten Lebenszyklus nur eine einzige Knotenidentität generieren kann.
Immun gegen Rechenleistungsangriffe: VDF ist nicht parallelisierbar; die Höhe der Rechenleistung beeinflusst nicht den Ertrag pro Zeiteinheit.
Immun gegen Diebstahl: Der private Schlüssel der Brieftasche steht unter der vollständigen Kontrolle des Nutzers; das System speichert keinerlei private Schlüssel.
Immun gegen Doppelausgaben: Time Coin kann nur zwischen konformen Brieftaschen peer-to-peer übertragen werden und kann nicht unabhängig von seiner entsprechenden Brieftasche existieren.
Immun gegen einen 51-%-Rechenleistungsangriff: Um 51 % der Ausgaberechte zu erlangen, müsste man 51 % der intelligenten Geräte weltweit kontrollieren, was wirtschaftlich nicht machbar ist.

5. Forks und Evolution
Dieses Protokoll verbietet keine Forks. Jeder Fork, der auf diesem Protokoll basiert, ist legal, und die Nutzer können frei wählen, welche Chain sie verwenden möchten.

Forks sind der Selbstentwicklungsmechanismus des Systems. Wenn ein Fork die Regeln dieses Protokolls modifiziert und die Anerkennung von mehr Nutzern erhält, wird er de facto zur Haupt-Chain. Alle Forks, die von den Nutzern nicht anerkannt werden, werden auf natürliche Weise aussterben, da keine Knoten sie betreiben.
Keine Einzelperson oder Organisation hat das Recht zu bestimmen, welche Chain „offiziell“ ist; der einzige Schiedsrichter ist die freie Wahl aller Nutzer.

Ein Gerät kann zu einem bestimmten Zeitpunkt nur eine VDF berechnen. Wenn daher ein Gerät zwei oder mehr Zeit-Fork-Brieftaschen gleichzeitig installiert, können die überzähligen Brieftaschen aufgrund der Nichtparallelisierbarkeit der Rechenleistung keine gültigen Zeitnachweise erzeugen und werden auf Protokollebene direkt als ungültig eingestuft.

Absolute Isolierung der Zeitdimension: Die Zeitmaßstäbe der einzelnen Fork-Chains sind voneinander unabhängig; ein Time Coin besitzt nur innerhalb der Zeitkette, in der er entstanden ist, Umlauflegitimität. Jegliches Cross-Chain-Transferverhalten kann auf kryptografischer Ebene keine kontinuierliche Kausalkette von PUF-Signaturen erzeugen und kommt faktisch einer physischen Zerstörung und Neuerzeugung gleich. Es besteht keine Möglichkeit des Cross-Chain-Umlaufs.

Alle Time Coins, die auf diesem Protokoll basieren, sowie deren Forks, müssen vollständig quelloffen sein, um die Authentizität und Konformität ihrer Protokollimplementierung überprüfen zu können.

6. Philosophische Deklaration des Time Coin
Absolute Dezentralisierung: Die vollständige Auflösung der Macht und die Geburt eines selbst-evidenten Systems
Time Coin strebt nicht nach Dezentralisierung, denn in der zugrunde liegenden Architektur von Time Coin existiert der Begriff „Zentrum“ überhaupt nicht. Alle bisherigen Währungssysteme, unabhängig von ihrer technischen Verpackung, konnten sich nie von drei impliziten höchsten Mächten befreien: dem Ausgaberecht, dem Buchführungsrecht und dem Regelentscheidungsrecht. Time Coin löst durch die starren Beschränkungen von Physik und Mathematik diese drei Mächte vollständig auf und gibt sie an jeden einzelnen unabhängigen Knoten zurück.

1. Die Auflösung des Ausgaberechts: Von „Gewährung durch Dritte“ zu „Selbstbeweis durch Zeit“
Im Time-Coin-Netzwerk besitzt kein Subjekt das Privileg, Währung auszugeben. Der Akt der „Ausgabe“ selbst wird zu dem objektiven physikalischen Phänomen herabgestuft: „ein physisches Gerät, das online Zeit verstreichen lässt“.
Keine Miner-Blockbelohnungen erforderlich, kein Staking für Zinserträge. Ihr Gerät existiert, die Zeit vergeht, die VDF-Berechnung wird abgeschlossen, und die Münze entsteht „nativ“ in Ihrem Gerät. Time Coin hat keinen Emittenten, nur Zeugen der Zeit.

2. Die Auflösung des Buchführungsrechts: Von „globaler Abhängigkeit“ zu „eine Münze, ein Beweis“
Traditionelle Blockchains sind darauf angewiesen, dass alle Knoten des Netzwerks gemeinsam ein „Hauptbuch“ führen, was bedeutet, dass die Legitimität Ihres Vermögens von der Anerkennung Fremder abhängen muss.
Der „eine Münze, ein Hauptbuch“-Mechanismus von Time Coin durchtrennt die Abhängigkeit von einem globalen Hauptbuch vollständig. Jeder Time Coin trägt von sich aus eine unveränderliche Kausalkette; seine Legitimität hängt nicht von den Aufzeichnungen irgendwelcher externen Knoten ab, sondern allein von der Kontinuität seiner eigenen Historie und den physischen PUF-Signaturen jedes einzelnen Besitzers in der Kette. Andere können weder Ihre Bücher für Sie führen noch Ihr Hauptbuch manipulieren.

3. Die Auflösung des Regelentscheidungsrechts: Von „Code-Diktatur“ zu „Echtzeit-Emergenz“
Im Time-Coin-Protokoll liegt die Anpassungsgewalt für den einzigen variablen Parameter (die Länge des Konsenszyklus) nicht in den Händen irgendeines Entwicklers, einer Stiftung oder eines Super-Knotens. Sie wird vollständig von allen aktiven Knoten in jedem Herzschlagzyklus durch gewichtete Abstimmung in Echtzeit errechnet.
Es gibt keine Anträge, keine Abstimmungstage, keine Community-Governance-Komitees. Die Regeln des Systems emergieren in Echtzeit selbstadaptiv, ähnlich der Fließgeschwindigkeit von Wasser, basierend auf der aktuellen Knotenanzahl. Time Coin hat keinen Herrscher, nur die Selbstkonsistenz der Algorithmen auf physikalischer Ebene.

7. Schlussfolgerung
Time Coin ist kein Ersatz für Bitcoin, sondern die Vollendung von Bitcoin.
Bitcoin hat die „Unantastbarkeit des Bestands“ verwirklicht.
Time Coin verwirklicht die „faire Teilhabe am Zuwachs“ und die „vollständige Kettentransparenz“.
Time Coin versucht nicht, Fiatgeld zu ersetzen oder Staaten zu beseitigen, sondern wartet auf die Ankunft der menschlichen Gemeinschaft. Es befiehlt niemandem, irgendetwas zu tun, und verbietet niemandem, irgendetwas zu tun. Es bietet lediglich den grundlegendsten Rahmen und überlässt es dann der gesamten Menschheit, selbst zu verhandeln, sich selbst zu regulieren und die Zukunft selbst zu gestalten.
Time Coin hat keine neuen Regeln geschaffen; es hat lediglich die grundlegendsten Gesetze des Universums – „das Vergehen der Zeit, die Unumkehrbarkeit von Kausalität“ – in Code geschrieben.

Dies ist „Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei“.

Das ist Tian zhi dao.

Dieses Weißbuch ist das einzige offizielle normative Dokument für das Time-Coin-Protokoll. Dieses Protokoll hat keinen offiziellen Code, keine offizielle Implementierung, keine offizielle Website, keinen Gründer und keinerlei Form von offizieller Organisation. Jede Entität kann dieses Protokoll frei implementieren. Alle Protokollimplementierungen, die den Regeln dieses Weißbuchs entsprechen, sind gültige Time-Coin-Protokolle.
Denn wahre Gerechtigkeit braucht keinen Vater.

Unterzeichnet: Dao Heng Wu Ming

------------------------------------------------------------------------

[Русский]

Резюме
В данной статье предлагается первая в истории человечества децентрализованная денежная система, основанная исключительно на времени. Система реализует базовый механизм «одно устройство — один голос — один кошелёк» на основе физически неклонируемых функций (PUF), гарантирует неподдельность времени за счёт верифицируемых функций задержки (VDF) и опирается на блокчейн Биткойна для обеспечения абсолютной безопасности и полной прозрачности всей цепочки.
Единственным основанием для эмиссии Тайм-Коина является верифицируемое онлайн-время. Любой субъект, обладающий подключаемым к сети интеллектуальным устройством, затрачивая равное количество верифицируемого времени, получает равное количество Тайм-Коин. Никаких капитальных порогов, никаких технических порогов, никаких порогов идентичности. Единственным способом изменения каких-либо параметров системы является голосование всех узлов в реальном времени по принципу «один человек — один голос».
Тайм-Коин не пытается сконструировать справедливость; он сам является справедливостью. Он не пытается скрыть какую-либо информацию; он сам есть полная прозрачность. Он не пытается решать проблемы; он позволяет проблемам самоустраняться.

1. Проблема
С момента появления Биткойна все криптовалюты не смогли решить две фундаментальные проблемы:
Монополия капитала на право денежной эмиссии: в механизме PoW капитал может монополизировать право на ведение реестра и эмиссию, покупая вычислительные мощности; в механизме PoS капитал может монополизировать право на стейкинг и эмиссию, владея токенами; все прочие механизмы консенсуса в конечном итоге превращаются в игру капитала.
Эксплуатация, вызванная информационной асимметрией: история обращения и потоки денежных средств скрыты, что позволяет процветать отмыванию денег, мошенничеству и спекуляциям.
Корень проблемы в том, что все подобные валюты пытаются искать справедливость в пространственном измерении и сохраняют искусственно созданные информационные барьеры.
Единственный ресурс, который нельзя купить за капитал, нельзя ускорить и нельзя подделать, — это время.
Единственная процедура, способная полностью устранить эксплуатацию, — это полная, безусловная прозрачность.

2. Три незыблемых основных правила
Весь свод правил Тайм-Коина состоит только из следующих трёх статей. Не существует никаких исключений, никаких патчей и никаких скрытых положений.

Правило первое: Одно устройство — один голос — один кошелёк
Любое отдельное физическое вычислительное устройство обладает и может обладать только одной идентификацией узла и одним привязанным кошельком; эта связь, однажды установленная, не может быть расторгнута. Каждый узел может получить и может получить только один Тайм-Коин за один цикл консенсуса.
Идентификация узла автоматически генерируется из встроенного в устройство чипа физически неклонируемой функции (PUF) и хеша высоты блока Биткойна. Она глобально уникальна и неповторима. Сброс системы приведёт к безвозвратной потере кошелька; можно будет лишь сгенерировать новый кошелёк.
Приватный ключ кошелька физически выводится на аппаратном уровне чипом PUF и никогда не существует вне чипа в какой-либо цифровой форме (например, мнемоническая фраза или шифротекст). Контроль пользователя над кошельком равнозначен абсолютному владению физическим устройством; не существует «независимого хранения», отделённого от устройства.
Когда PUF устройства выходит из строя из-за старения, повреждения или по любой другой причине, этот узел навсегда умирает и прекращает генерировать Тайм-Коины; уже имеющиеся в его кошельке Тайм-Коины будут навечно заморожены вместе с этим узлом и выведены из обращения. Никто не может их передать или восстановить. При старении устройства существующие в кошельке Тайм-Коины можно заранее перевести на любой другой действительный узел. При потере устройства единственный способ восстановления — найти само устройство.
Любая операция, такая как сброс системы, форматирование устройства или замена чипа, безвозвратно уничтожит локально хранящийся приватный ключ кошелька и все данные Тайм-Коина.
Даже на одном и том же физическом устройстве идентификация узла и кошелёк, сгенерированные после сброса, являются совершенно новыми и независимыми, не имеющими никакой связи с предыдущей идентификацией и кошельком.
Все Тайм-Коины исходного кошелька, навсегда потеряв возможность получить авторизацию подписи от исходного чипа PUF, никогда больше не смогут участвовать ни в какой транзакции, что равносильно физическому уничтожению. Это как бросить наличные в огонь: сами деньги не исчезли, но они никогда больше не смогут быть использованы кем-либо.
Чисто программные виртуальные среды (без физического чипа PUF) не могут сгенерировать действительную идентификацию узла и кошелёк.
Права узлов всех устройств абсолютно равны: Raspberry Pi за 50 долларов = телефон за 10 000 долларов = суперкомпьютер за 100 миллионов долларов.
Любое устройство в любом месте получает абсолютно одинаковый доход за единицу времени.

Блокировка временной линии:
Экономическая жизнь физического устройства обладает абсолютной исключительностью. Когда чип PUF устройства впервые активируется любым совместимым клиентом на основе данного протокола, внутри защищённого анклава PUF генерируется необратимый флаг «блокировки протокола».
Будучи однажды заблокирован, этот чип PUF на физическом уровне абсолютно отказывается выполнять рукопожатие или вычисление подписи с любым другим клиентом форка протокола.
В течение жизненного цикла одного физического устройства оно может и неизбежно будет участвовать только в доказательстве времени одной форк-цепи Тайм-Коина. Если субъект-узел намеревается участвовать в другой форк-цепи, единственным законным путём является приобретение другого совершенно нового, неактивированного физического устройства.
Данный протокол лишает одно физическое устройство права одновременно владеть несколькими валютами, основанными на времени. Выбор временного правила должен быть оплачен соответствующей стоимостью физического оборудования.

Правило второе: Временной стандарт · Полная прозрачность цепочки
Единственным основанием для эмиссии Тайм-Коина является верифицируемое время вычислений в сети. Полный жизненный цикл каждого отдельного Тайм-Коина будет навсегда записан в неизменяемом виде.
Никакого предварительного майнинга, никаких вознаграждений основателям, никаких институциональных долей, никаких форм предварительного распределения.
Общее предложение не имеет фиксированного верхнего предела; объём эмиссии автоматически пропорционален количеству активных узлов во всей сети.
Никакой компенсации за офлайн-время; только узлы, непрерывно выполняющие вычисления VDF в сети, могут получать Тайм-Коины.
Все узлы одновременно вычисляют одну и ту же верифицируемую функцию задержки (VDF), основываясь на одном и том же хеше блока Биткойна.
Неподдающаяся распараллеливанию природа VDF гарантирует, что единственная разница во времени завершения вычислений между всеми узлами обусловлена физическими отклонениями.
Все устройства, завершившие вычисление досрочно, должны дожидаться общесетевого оповещения следующего цикла консенсуса, чтобы продолжить.
Цикл консенсуса представляет собой целое кратное количества вычислений VDF и определяется путём взвешенного голосования всех узлов в реальном времени.
За каждый завершённый цикл консенсуса непрерывного вычисления VDF все активные узлы одновременно получают один и только один Тайм-Коин.
Каждый отдельный Тайм-Коин навсегда зафиксирует высоту блока своего рождения и PUF-идентификатор породившего его устройства.
Каждая транзакция каждого Тайм-Коина навсегда фиксирует время транзакции и идентификаторы кошельков отправителя и получателя, реализуя одну независимую учётную книгу на каждый Тайм-Коин.
Право собственности на Тайм-Коин может быть передано только посредством пирингового перевода; любой экспорт, копирование или резервное копирование недействительны.
Каждый Тайм-Коин неотъемлемо несёт в себе полную цепочку истории транзакций; любая передача права собственности обязана добавить новую запись транзакции в цепочку истории самого этого Тайм-Коина.
Каждая транзакция должна быть подтверждена подписью чипа PUF отправляющего устройства, прежде чем она вступит в силу.
Каждый Тайм-Коин является минимальной единицей, неделим и может обращаться только в целых кратных числах.
Любые данные Тайм-Коина, покинувшие свой соответствующий кошелёк, теряют полную цепочку истории, не могут быть проверены узлами всей сети и считаются недействительной валютой.

Определение Тайм-Коина: Единица и обращение
Минимальная единица: 1 Тайм-Коин
Тайм-Коин — это неделимая, неразрезаемая, не подлежащая дроблению полноценная единица стоимости, соответствующая уникальной временной выработке одного устройства в течение одного цикла консенсуса.

Необъединяемая онтология Тайм-Коина
Любое множество Тайм-Коин не может быть объединено, слито или сжато. Каждый Тайм-Коин от своего рождения до окончательного прекращения обращения постоянно сохраняет независимую идентичность и независимую цепочку истории.

Только целочисленные транзакции
Все переводы, платежи и обмены могут осуществляться только целыми количествами: 1, 2, 3… Никаких десятичных знаков, никакой сдачи через дробление.

История только дополняется, никогда не сокращается; только продолжается, никогда не изменяется
История транзакций каждого Тайм-Коина может лишь пополняться новыми записями; её нельзя удалять, подделывать, перезаписывать, объединять или упрощать.

Покидание кошелька означает смерть
Единственной законной средой существования Тайм-Коина является аппаратный защищённый анклав в области памяти «горячего кошелька», защищённый аппаратным шифрованием чипа PUF устройства.

Запрет экспорта: Данные Тайм-Коина и производные от них приватные ключи категорически запрещено покидать защищённый анклав PUF в какой бы то ни было форме (файл экспорта, скриншот, копирование-вставка, передача открытым текстом по сети) и попадать в память обычной операционной системы или на внешнее хранилище. Как только происходит такое понижение уровня безопасности, немедленно срабатывает «разрыв истории», и его внутреннее состояние мгновенно помечается системой как «исторический разрыв».

Запрет обратного ввода: Любая попытка вернуть данные Тайм-Коина, которые хоть раз покидали среду PUF, обратно в кошелёк, будет автоматически распознана и отклонена всеми узлами сети.

Фрагментация означает недействительную валюту: Когда инициируется транзакция, PUF получателя при приёме данных проверяет причинную цепочку этого Тайм-Коина. Если в цепочке обнаруживаются следы сращивания, не порождённые физической подписью PUF, или выявляются такие явления, как инверсия временных меток или разрывы хешей, это считается «исторической фрагментацией». Тайм-Коин, вызвавший тревогу, отвергается всей сетью и считается недействительным.

Легитимное пиринговое рукопожатие анклавов: Единственным разрешённым «трансфером» является «рукопожатие добавления состояния», осуществляемое напрямую между защищёнными анклавами PUF двух устройств, находящихся в сети, по зашифрованному каналу. Пакет данных Тайм-Коина ни при каких обстоятельствах не должен проходить через какой-либо сторонний сервер или не-PUF-среду.

Транзакции — это добавление состояния, а не перемещение данных
Когда пользователь меняет старый телефон на новый, по ощущениям кажется, что «Тайм-Коины перевелись на новый телефон», но в основополагающей логике:
Защищённый анклав PUF старого телефона физически подписывает и добавляет в конец локальной причинной цепочки Тайм-Коина запись: «Контроль передан хешу PUF нового телефона».
Затем старый анклав PUF устанавливает зашифрованный пиринговый туннель с новым анклавом PUF и напрямую проталкивает эти «полные данные Тайм-Коина с обновлённым хвостом» в анклав PUF нового телефона. На протяжении всего процесса данные Тайм-Коина ни разу не касаются какой-либо обычной операционной системы, достигая абсолютной изоляции безопасности.

Единственная задача блокчейна: нотариальное удостоверение времени
Базовая сеть этого протокола (такая как блокчейн Биткойна) не выполняет функцию «ведения реестра»; она лишь играет роль «абсолютного нотариуса времени».
Всякий раз, когда Тайм-Коин внутренне добавляет запись о передаче, существование блокчейна служит исключительно для предоставления «неизменяемого внешнего хеша временной метки» для внутренней причинной цепочки Тайм-Коина, помогая доказать, что его история не была откачена. Блокчейн не хранит никаких транзакционных данных или пользовательской информации Тайм-Коина.

Правило третье: Всеобщее управление в реальном времени
Единственным механизмом корректировки какого-либо системного параметра является непрерывное взвешенное голосование всех активных узлов в реальном времени. Последствия любой корректировки несут сообща все узлы.
Единственным регулируемым параметром является продолжительность цикла консенсуса.
Система предустанавливает 15 вариантов экспоненциально растущих циклов консенсуса; любой узел может в любой момент выбрать любой вариант, а также в любой момент изменить свой выбор.
Голоса, как часть состояния узла, автоматически распространяются по всей сети вместе с пульсом узла.
Все узлы независимо вычисляют и верифицируют результат общесетевого голосования, принимая доли голосов топ-10 вариантов, набравших наибольшее общее число голосов, для вычисления взвешенного среднего, получая таким образом текущий действующий цикл консенсуса.
Действующий цикл консенсуса автоматически обновляется и немедленно вступает в силу каждые 10 минут. Никаких периодов голосования, никаких процессов утверждения, никакого центрального статистического узла.
Учётные данные, сгенерированные без принятия консенсуса либо путём самовольного искажения временного цикла, не обладают свойствами Тайм-Коина внутри данной временной цепи, считаются недействительными данными и будут напрямую отвергнуты всеми узлами сети для приёма, верификации и транзакций.
Консенсус может быть сформирован при наличии в сети двух и более устройств.
Регулировка любого иного параметра является незаконной.

3. Механизм саморегуляции
Тайм-Коин не требует какого-либо вмешательства человека; это идеально самобалансирующаяся система.

Автоматическое растворение капитальных атак
Если капитальная сторона массово закупает устройства, пытаясь монополизировать право эмиссии, сработают следующие многоуровневые автоматические балансировочные механизмы:
Увеличение общего количества узлов сети → объём эмиссии Тайм-Коина синхронно растёт → цена одного Тайм-Коина автоматически падает.
Все узлы голосуют за удлинение цикла консенсуса → доход за единицу времени у всех узлов пропорционально снижается.
Жёсткие затраты капитальной стороны на электричество, пропускную способность, помещения, персонал и прочее остаются неизменными → прибыль резко сокращается.
Крупномасштабные майнинговые фермы столкнутся с экспоненциально растущими издержками на ручные транзакции; чем больше масштаб, тем тяжелее убытки.
Когда доход падает ниже издержек, капитальная сторона автоматически отключается и уходит → система возвращается в равновесие.
Частные пользователи практически не затрагиваются (интеллектуальные устройства и без того постоянно находятся в работе, предельные издержки участия в качестве узла практически нулевые).

Автоматическая стабильность цены
Стоимость Тайм-Коина навечно привязана к эталону «1 Тайм-Коин = верифицируемое человеческое время 1 цикла консенсуса». Его цена не будет стабилизироваться вблизи эксплуатационных расходов; напротив, эксплуатационные расходы будут автоматически стабилизироваться вблизи цены Тайм-Коина.
Цена Тайм-Коина растёт → больше пользователей запускают узлы → предложение увеличивается → цена падает обратно.
Цена Тайм-Коина падает → спекулянты уходят → предложение сокращается → цена восстанавливается.
Это механически предотвращает резкие скачки, обвалы и спекулятивный простор; цена Тайм-Коина по своей сути есть справедливая цена времени.

Автоматическая изоляция токсичных активов
Все истории транзакций полностью открыты и прозрачны; рынок автоматически осуществит отсеивание и изоляцию:
Тайм-Коины, участвовавшие в незаконных транзакциях, будут спонтанно отвергаться большинством торговцев и пользователей.
Любой субъект рынка может автономно отказаться от любого Тайм-Коина, вовлечённого в незаконную транзакцию, без необходимости одобрения какой-либо третьей стороны.
Не существует единого, принудительного чёрного списка; все фильтрационные действия являются добровольными и рыночно-ориентированными.

4. Безопасность
Безопасность Тайм-Коина совместно гарантируется физикой и математикой:
Иммунитет к атакам Сивиллы: комбинация PUF и хеша высоты блока Биткойна гарантирует, что одно физическое устройство может сгенерировать только одну уникальную идентификацию узла за весь свой жизненный цикл.
Иммунитет к атакам вычислительной мощностью: VDF не поддаётся распараллеливанию; уровень вычислительной мощности не влияет на доход за единицу времени.
Иммунитет к краже: приватный ключ кошелька полностью контролируется пользователем; система не хранит никаких приватных ключей.
Иммунитет к двойной трате: Тайм-Коин может быть переведён только пиринговым способом между совместимыми кошельками и не может существовать независимо, отдельно от своего соответствующего кошелька.
Иммунитет к атаке 51% вычислительной мощности: получение 51% прав эмиссии потребовало бы контроля над 51% интеллектуальных устройств планеты, что экономически неосуществимо.

5. Форки и эволюция
Данный протокол не запрещает форки. Любой форк, основанный на этом протоколе, является легальным, и пользователи могут свободно выбирать, какую цепь использовать.

Форки — это механизм самоэволюции системы. Если форк изменяет правила данного протокола и получает признание большего числа пользователей, он становится де-факто основной цепью. Все форки, не признанные пользователями, естественным образом исчезнут из-за отсутствия работающих на них узлов.
Ни один человек и ни одна организация не имеют права определять, какая цепь является «официальной»; единственный арбитр — свободный выбор всех пользователей.

Одно устройство в каждый момент времени может вычислять только одну VDF. Поэтому если одно устройство установит два или более кошельков временных форков одновременно, то из-за невозможности распараллеливания вычислений лишние кошельки не смогут выдавать действительные временные доказательства и будут напрямую признаны недействительными на уровне протокола.

Абсолютная изоляция временного измерения: временные масштабы различных форк-цепей взаимно независимы; Тайм-Коин обладает легитимностью обращения только внутри той временной цепи, в которой он родился. Любое кросс-чейн поведение передачи не может породить непрерывную причинную цепочку PUF-подписей на криптографическом уровне, что фактически равнозначно физическому уничтожению и повторной генерации. Возможность кросс-чейн обращения отсутствует.

Все Тайм-Коины, основанные на этом протоколе, и их форки должны быть полностью с открытым исходным кодом, чтобы можно было проверить подлинность и соответствие их реализации протокола.

6. Философская декларация Тайм-Коина
Абсолютная децентрализация: Полное растворение власти и рождение самоочевидной системы
Тайм-Коин не стремится к децентрализации, ибо в основополагающей архитектуре Тайм-Коина понятие «центр» попросту отсутствует. Все прошлые денежные системы, какой бы ни была их технологическая оболочка, никогда не могли избежать трёх неявных верховных властей: права эмиссии, права ведения реестра и права принятия решений о правилах. Посредством жёстких ограничений физики и математики Тайм-Коин полностью «растворяет» эти три власти, возвращая их каждому отдельному независимому узлу.

1. Растворение права эмиссии: от «дарования третьей стороной» к «самодоказательству временем»
В сети Тайм-Коин ни один субъект не обладает привилегией эмитировать валюту. Сам акт «эмиссии» низводится до объективного физического явления «истечения времени, пока физическое устройство находится в сети».
Не требуется ни наград майнерам за блоки, ни стейкинга для получения процентов. Ваше устройство существует, время идёт, вычисление VDF завершено, и монета «рождается» нативно внутри вашего устройства. У Тайм-Коина нет эмитента, есть только свидетели времени.

2. Растворение права ведения реестра: от «глобальной зависимости» к «одна монета — одно доказательство»
Традиционные блокчейны полагаются на то, что все узлы сети совместно ведут одну «главную книгу», а это означает, что легитимность ваших активов должна зависеть от признания незнакомцев.
Механизм Тайм-Коина «одна монета — одна учётная книга» полностью разрубает зависимость от глобального реестра. Каждый Тайм-Коин неотъемлемо несёт в себе неизменяемую причинную цепочку; его легитимность не зависит от записей какого-либо внешнего узла, но исключительно от непрерывности его собственной истории и физических PUF-подписей каждого из его владельцев в цепочке. Другие не могут ни вести ваши книги за вас, ни подделать ваш реестр.

3. Растворение права принятия решений о правилах: от «кодовой диктатуры» к «возникновению в реальном времени»
В протоколе Тайм-Коин власть корректировать единственный варьируемый параметр (продолжительность цикла консенсуса) не находится в руках какого-либо разработчика, фонда или суперузла. Она полностью вычисляется в реальном времени посредством взвешенного голосования всех активных узлов в течение каждого цикла пульсации.
Нет ни предложений, ни дней голосования, ни комитетов по управлению сообществом. Правила системы адаптивно самовозникают в реальном времени в зависимости от текущего количества узлов, подобно скорости течения воды. У Тайм-Коина нет правителя, есть только физическая самосогласованность алгоритмов.

7. Заключение
Тайм-Коин — это не замена Биткойна, а завершение Биткойна.
Биткойн реализовал «неприкосновенность существующего запаса».
Тайм-Коин реализует «справедливое разделение прироста» и «полную прозрачность всей цепочки».
Тайм-Коин не пытается заменить фиатные деньги, не пытается уничтожить государства, но ожидает прихода человеческого сообщества. Он никому не приказывает что-либо делать и никому не запрещает что-либо делать. Он просто предоставляет самый базовый каркас и затем позволяет всему человечеству самостоятельно договариваться, саморегулироваться и самим творить будущее.
Тайм-Коин не создал никаких новых правил; он просто вписал в код фундаментальнейшие законы вселенной — «течение времени, необратимость причинности».

Это и есть «Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei».

Это и есть Tian zhi dao.

Данная белая книга является единственным официальным нормативным документом протокола Тайм-Коин. У этого протокола нет ни официального кода, ни официальной реализации, ни официального веб-сайта, ни основателя, ни какой-либо формы официальной организации. Любое лицо может свободно реализовывать данный протокол. Все реализации протокола, соответствующие правилам настоящей белой книги, являются действительными протоколами Тайм-Коин.
Ибо истинная справедливость не нуждается в отце.

Подпись: Dao Heng Wu Ming

------------------------------------------------------------------------

[Latina]

Summarium
Hoc scriptum primum in generis humani historia systema monetarium mere temporale et decentralisatum proponit. Systema nuclearem mechanismum “unum instrumentum, una vox, unum marsupium” ope Functionum Physice non Clonabilium (PUF) efficit, temporis infalsificabilitatem per Functiones Morae Verificabiles (VDF) assequitur, et in catena Bitcoinica finalem securitatem perspicuitatemque omnis catenae obtinet.
Unicum fundamentum emissionis Nummi Temporis est tempus verificabile in rete. Quodlibet ens instrumentum intelligens conectibile possidens, impendens aequale tempus verificabile, aequalem copiam Nummorum Temporis accipit. Nullum limen capitale, nullum technicum, nullum identitatis. Sola ratio cuiuslibet parametri systematis mutandi est suffragatio realis omnium nodorum secundum principium “unus homo, una vox”.
Nummus Temporis aequitatem excogitare non temptat; est ipsa aequitas. Nullam informationem celare temptat; est ipsa perspicuitas summa. Problemata solvere non temptat; problemata sponte dissolvi sinit.

1. Problema
Ex quo Bitcoin natum est, omnes cryptomonetae duo problemata fundamentalia solvere nequiverunt:
Monopolium capitalis in ius monetam emittendi: sub mechanismo PoW, capitale per emptionem potentiae computatoriae potest monopolium tenere libri et ius emittendi; sub PoS, capitale per detentionem tokenorum potest monopolium tenere pignoris et ius emittendi; omnes ceteri consensus mechanismi demum in ludum capitalis evadunt.
Exploitio ex asymmetria informationis orta: historia circulationis fluxusque pecuniae obscurantur, permittens pecuniam sordidam, fraudes et speculativam actionem vigere.
Radix problematis in eo est quod omnes eiusmodi monetae aequitatem in dimensione spatiali quaerere temptant, et omnes impedimenta informationis artificiose designata retinent.
Sola res quae capitali emi non potest, accelerari non potest, nec falsificari, est tempus.
Solus modus qui exploitationem prorsus tollere potest est perspicuitas plena, sine condicione.

2. Tres Regulae Fundamentales et Inconcussae
Omnis canon Nummi Temporis his tribus solis articulis constat. Nullae exceptiones, nullae emendationes, nullae clausulae absconditae.

Regula Prima: Unum Instrumentum, Una Vox, Unum Marsupium
Quodvis singulare instrumentum computatorium physicum unicam identitatem nodalem et unum marsupium ligatum habet et habere potest; hoc vinculum, semel stabilitum, dissolvi non potest. Quisque nodus potest recipere et solum unum Numum Temporis recipere in unoquoque cyclo consensus.
Identitas nodi automatice generatur e chip PUF instrumento infixo et e hash altitudinis blocci Bitcoin. Est unica in orbe et non repetibilis. Systematis repositio amissionem perpetuam marsupii affert; novum tantum marsupium regenerari potest.
Clavis privata marsupii physice in strato hardware a chip PUF derivatur, nec umquam extra chip in ulla forma digitali (sicut phrases mnemonicae aut textus cifratus) exsistit. Potestas usoris super marsupium aequivalet possessioni absolutae instrumenti physici; nulla est “custodia independens” ab instrumento separata.
Cum PUF instrumenti ob vetustatem, damnum aut aliam causam deficit, ille nodus perpetualiter moritur et Nummorum Temporis generationem cessat; Nummi Temporis iam in marsupio suo exsistentes una cum nodo perpetuo congelantur, circulatione exeunt, nec transferri nec recuperari possunt ab ullo. Si instrumentum senescit, Nummi Temporis exsistentes in marsupium alium validum praeferri possunt. Si instrumentum amittitur, unica recuperandi ratio est ipsum instrumentum recuperare.
Quaelibet operatio qualis repositio systematis, formatio instrumenti vel chipis substitutio clavem privatam localiter repositam et omnia data Nummorum Temporis irreparabiliter delet.
Etiam in eodem instrumento physico, identitas nodi et marsupium post repositionem generata prorsus nova et independentia sunt, nullam relationem cum identitate et marsupio prioribus habent.
Omnes Nummi Temporis marsupii originalis, cum potestatem signaturam a chip PUF originali obtinendi perpetuo amiserint, numquam amplius ulla transactione participare possunt, quod physicae destructioni aequivalet. Hoc est quasi pecuniam numeratam in ignem conicere: ipsa pecunia non evanuit, sed numquam ab ullo adhiberi potest.
Mera programmata virtualia (sine chip PUF physico) identitatem nodalem et marsupium valida generare nequeunt.
Iura nodorum omnium instrumentorum omnino aequalia sunt: Raspberry Pi 50 dollariorum = telephonum 10 000 dollariorum = supercomputatrum 100 000 000 dollariorum.
Quodvis instrumentum, quovis loco, idem prorsus proventum per unitatem temporis accipit.

Claustrum Lineae Temporalis:
Vita oeconomica instrumenti physici exclusivitatem absolutam habet. Cum chip PUF instrumenti primum activatur ab ullo cliente congruente huic protocollo innixo, intra saeptum securum PUF irreversibile vexillum “claustri protocolli” generatur.
Semel clausus, ille chip PUF in strato physico absolute recusat ullum handshake aut computationem signaturae cum alio cliente furcae protocolli efficere.
Per cursum vitae unius instrumenti physici, potest et necessario tantummodo probationem temporis unius catenae furcae Nummi Temporis participare. Si entitas nodi intendit aliam catenam furcae participare, unica via licita est acquirere aliud instrumentum physicum omnino novum, non activatum.
Hoc protocollum unum instrumentum physicum iure privatiu detinendi plures monetas temporales simul privat. Electio regulae temporariae cum impensa hardware physicae correspondente solvenda est.

Regula Secunda: Mensura Temporis · Perspicuitas Omnis Catenae
Unicum fundamentum emissionis Nummi Temporis est tempus computatorium verificabile in linea. Integer vitae cyclus cuiusque Nummi Temporis immutabiliter et perpetuo notabitur.
Nulla prae-minatio, nulla praemia fundatoribus, nullae portiones institutionales, nulla ulla forma praedistributionis.
Nullus est finis superior fixus summae copiae; volumen emissionis automatice proportionale est numero nodorum activorum in omni rete.
Nulla compensatio pro tempore offline; solum nodi qui computationes continuas VDF online complent, Nummum Temporis recipere possunt.
Omnes nodi simul eandem Functionem Morae Verificabilem (VDF) computant, fundati in eodem hash blocci Bitcoin.
Natura non parallelisabilis VDF efficit ut sola differentia in tempore completionis inter omnes nodos sit ob variationem physicam.
Omnia instrumenta quae computationem praeveniunt, exspectare debent diffusionem retealem proximi cycli consensus ut pergant.
Cyclus consensus est multiplex integer numeri computationum VDF, determinatus per suffragationem ponderatam realem omnium nodorum.
Pro unoquoque cyclo consensus computationis continuae VDF completo, omnes nodi activi simul unum et unum tantum Numum Temporis accipiunt.
Quisque Nummus Temporis perpetuo notabit altitudinem blocci suae nativitatis et identificatorem PUF instrumenti generantis.
Quaeque transactio cuiusque Nummi Temporis perpetuo notat tempus transactionis et identificatores marsupiorum mittentis et recipientis, perficiens unum librum independentem pro Nummo Temporis.
Proprietas Nummi Temporis solum per translationem parem-ad-parem transferri potest; omnis forma exportationis, duplicationis vel salvamenti invalida est.
Quisque Nummus Temporis in se portat catenam completam historiae transactionum; quaelibet translatio proprietatis debet novum recordum transactionis catenae historiae ipsius Nummi Temporis addere.
Quaeque transactio debet signatura chip PUF instrumenti mittentis confirmari antequam vigorem obtineat.
Quisque Nummus Temporis est unitas minima, indivisibilis, et solum in multiplicibus integris transigi potest.
Quaevis data Nummi Temporis quae suum marsupium reliquerunt, catenam historicam integram amittunt, a nodis omnis retis verificari nequeunt, et pro moneta invalida habentur.

Definitio Nummi Temporis: Unitas et Circulatio
Unitas minima: 1 Nummus Temporis
Nummus Temporis est unitas valoris plena, indivisibilis, inscindibilis, non subdividenda, respondens unico proventui temporis unius instrumenti intra unum cyclum consensus.

Ontologia Nummi Temporis Non Unificabilis
Quilibet plures Nummi Temporis nec fundi, nec coniungi, nec comprimi possunt. Quisque Nummus Temporis, a nativitate usque ad finem circulationis, perpetuo identitatem independentem et catenam historiae independentem conservat.

Transactiones Tantum Integrae
Omnes translationes, solutiones et permutationes solum in quantitatibus integris 1, 2, 3... fieri possunt; nullae decimales, nulla moneta per divisionem reddita.

Historia Tantum Appenditur, Numquam Mutatur
Historia transactionum cuiusque Nummi Temporis tantummodo nova acta accipere potest; non potest deleri, corrumpi, superscribi, unificari aut simplicificari.

Exire e Marsupio Significat Mortem
Unicus ambitus legitimus exsistentiae Nummi Temporis est saeptum securum hardware intra zonam memoriae “marsupii calidi”, protegentis per encryptationem strati hardware chipis PUF instrumenti.

Prohibitio Exportationis: Data Nummi Temporis eiusque claves privatae derivatae absolute vetantur exire saeptum securum PUF in ulla forma (fasciculus exportatus, captura monitorii, copiare et inserere, transmissio aperta per rete) et intrare in memoriam systematis operationis conventionalis aut in repositorium externum. Simul ac talis degradatio fit, “ruptura historiae” immediate desponsatur, et eius status internus a systemate instanter “historice ruptus” notatur.

Prohibitio Reimportationis: Quilibet conatus data Nummi Temporis, quae semel ambitum PUF reliquerunt, iterum in marsupium importare, a nodis totius retis automatice agnoscetur et recusabitur.

Fragmentatio Significat Monetam Invalidam: Cum transactio initiatur, PUF recipientis, recipiens data, catenam causalem illius Nummi Temporis verificat. Si in catena vestigia suturae inveniuntur non per signaturam physicam PUF generata, aut condiciones qualis inversio indicis temporis vel rupturae hash deteguntur, hoc “fragmentatio historiae” iudicatur. Nummus Temporis qui terrorem excitat, ab omni rete recusatur et pro invalido habetur.

Legitimum Handshake Saeporum Par-ad-Parem: Unica “translatio” permissa est “handshake appendendi status”, effecta directe inter saepta secura PUF duorum instrumentorum in linea per canalem encryptatum. Fasciculus datorum Nummi Temporis sub nulla condicione per ullum servitorem tertium aut ambitum non-PUF transire debet.

Transactiones Sunt Appendere Statum, Non Movere Data
Cum usor telephonum vetus pro novo substituit, experientia sentitur quasi “Nummi Temporis ad novum telephonum translati sunt”, sed in logica subiacente:
Saeptum securum PUF veteris telephoni physice signat et in fine catenae causalis Nummi Temporis localis actum appendit: “Imperium translatum ad hash PUF novi telephoni”.
Deinde vetus saeptum PUF canalem encryptatum par-ad-parem cum novo saepto PUF statuit et haec “data integra Nummi Temporis cum fine renovato” directe in saeptum PUF novi telephoni impellit. Per omnem cursum, data Nummi Temporis nullum systema operationis conventionalem tangunt, absolutam segregationem securitatis attingentes.

Unicum Munus Catena Bitcoinicae: Notariatus Temporalis
Retis subiacens huius protocolli (qualis catena Bitcoinica) munus “libri faciendi” non assumit; solummodo functionem “notarii temporis absoluti” implet.
Quoties Nummus Temporis interne actum translationis appendit, exsistentia catenae Bitcoinicae unice servit ad praebendum “hash temporis externum immutabilem” catenae causali internae Nummi Temporis, ad adiuvandum probandum historiam eius non esse revolutam. Catena Bitcoinica nulla data transactionis aut informationem utentium Nummi Temporis recondit.

Regula Tertia: Gubernatio Universalis Temporis Realis
Unicus modus ullum parametrum systematis accommodandi est suffragatio continua ponderata omnium nodorum activorum in tempore reali. Consequentiae cuiuslibet accommodationis ab omnibus nodis communiter feruntur.
Unicus parametrus accommodabilis est duratio cycli consensus.
Systema praestituit 15 optiones cyclorum consensus exponentialiter crescentium; quilibet nodus potest quamlibet optionem quolibet momento eligere, et etiam quamlibet electionem suam mutare quolibet momento.
Suffragia, ut pars status nodi, automatice per omne rete cum pulsatione cordis nodi diffunduntur.
Omnes nodi independenter computant et verificiant eventum suffragationis retealis, accipientes portiones suffragiorum 10 optionum cum summis suffragiis totalibus ad computandum medium ponderatum, sic obtinentes currentem cyclum consensus efficacem.
Cyclus consensus efficax automatice renovatur et immediate vigorem obtinet singulis 10 minutis. Nulli periodi suffragationis, nulli processus approbationis, nullus nodus statisticus centralis.
Documenta probatoria sine acceptatione consensus aut per adulterationem cycli temporis generata, intra hanc catenam temporalem proprietates Nummi Temporis non possident, pro datis invalidis habentur, et a nodis totius retis directe recusantur pro receptione, verificatione et transactione.
Consensus iam cum duobus vel pluribus instrumentis in linea formari potest.
Accommodatio cuiuslibet alterius parametri illicita est.

3. Mechanismus Autoregulativus
Nummus Temporis nulla interventione humana indiget; est systema perfecte autoaequilibrium.

Dissolutio Automatica Impetus Capitalis
Si qua pars capitalis magnum numerum instrumentorum emit temptans monopolium emissionis, sequentes mechanismi autoaequilibrii multistrati excitabuntur:
Numerus totalis nodorum retis augetur → volumen emissionis Nummi Temporis synchronice crescit → pretium singuli Nummi Temporis automatice cadit.
Omnes nodi suffragantur cyclum consensus prorogandum → proventus per unitatem temporis omnium nodorum proportionaliter deminuitur.
Sumptus rigidi capitalis partis pro electricitate, fascia, spatio, labore manuali etc. immutati manent → lucrum drastice minuitur.
Magnae fundi cuniculationis obviam ibunt sumptibus manualis transactionis exponentialiter crescentibus; quo maior scala, eo gravius damnum.
Cum reditus infra sumptus cadit, pars capitalis automatice clauditur et recedit → systema ad aequilibrium redit.
Usatores singulares paene omnino non afficiuntur (instrumenta intelligentia iam diu in operatione permanent, sumptus marginalis participandi ut nodus prope nullus est).

Stabilitas Pretii Automatica
Valor Nummi Temporis perpetuo ancoratus est in basi “1 Nummus Temporis = tempus humanum verificabile 1 cycli consensus”. Eius pretium non stabiliscetur prope sumptus operationales; contra, sumptus operationales automatice stabilientur prope pretium Nummi Temporis.
Pretium Nummi Temporis ascendit → plures usores nodos exercent → copia crescit → pretium recidit.
Pretium Nummi Temporis descendit → speculatores discedunt → copia decrescit → pretium resurgit.
Hoc mechanismo intrinsice vitantur impetuosi saltus, ruinae et spatium speculationis; pretium Nummi Temporis re vera est pretium iustum temporis.

Isolatio Automatica Bonorum Toxicorum
Omnes historiae transactionum perfecte apertae et perspicuae sunt; mercatus automatice cribrationem et isolationem efficiet:
Nummi Temporis qui transactionibus illicitis interfuerunt a plerisque mercatoribus et usoribus sponte recusabuntur accipi.
Quislibet actor mercatus potest autonome quemlibet Numum Temporis implicatum in transactione illicita recusare, sine indigentia approbationis alicuius tertii.
Nulla est lista nigra unificata, coacta; omnes actiones filtrationis voluntariae et mercatu actae sunt.

4. Securitas
Securitas Nummi Temporis a physica et mathematica coniunctim praestatur:
Immunitas contra Impetus Sybiles: Coniunctio PUF et hash altitudinis blocci Bitcoin efficit ut unum instrumentum physicum per totum suum cyclum vitae unicam tantum identitatem nodalem generare possit.
Immunitas contra Impetus Potentiae Computatoriae: VDF non est parallelisabilis; planities potentiae computatoriae proventum per unitatem temporis non afficit.
Immunitas contra Furtum: Clavis privata marsupii a usore plene regitur; systema nullas claves privatas recondit.
Immunitas contra Duplicem Impensam: Nummus Temporis solum inter marsupia conformia par-ad-parem transferri potest et non potest separatim a suo marsupio correspondente exsistere.
Immunitas contra Impetum 51% Potentiae Computatoriae: Acquirere 51% iurium emissionis requireret potestatem super 51% instrumentorum intelligentium orbis terrarum, quod oeconomice infeasibile est.

5. Furcae et Evolutio
Hoc protocollum furcas non prohibet. Quaelibet furca huic protocollo innixa legitima est, et usores possunt libere eligere quam catenam adhibere.

Furcae sunt mechanismus autoëvolutionis systematis. Si qua furca regulas huius protocolli modificavit et maiorem numerum usorum agnoscit, tunc de facto catena principalis fiet. Omnes furcae ab usoribus non agnitae naturaliter peribunt deficientibus nodis eas exercentibus.
Nullus homo nec ulla organizatio ius habet determinandi quaenam catena “officialis” sit; unicus arbiter est libera electio omnium usorum.

Unum instrumentum unoquoque momento unicam tantum VDF computare potest. Itaque, si unum instrumentum duo vel plura marsupia furcae temporalis simul installat, ob impossibilitatem parallelisationis computationis, marsupia redundantia valida testimonia temporis producere nequeunt et in strato protocolli directe invalida iudicantur.

Absoluta Isolatio Dimensionis Temporalis: Scalae temporales diversarum catenarum furcae inter se independentes sunt; Nummus Temporis tantummodo intra catenam temporalem ubi natus est circulationis legitimitatem habet. Quilibet motus translationis inter catenas nequit catenam causalem continuam signaturarum PUF generare in plano cryptographico, quod efficaciter aequivalet destructioni physicae et regenerationi. Possibilitas circulationis inter catenas non exsistit.

Omnes Nummi Temporis huic protocollo innixae eorumque furcae omnino apertae fontis esse debent, ut authenticitas et conformitas eorum implementationis protocolli verificari possint.

6. Declaratio Philosophica Nummi Temporis
Decentralisatio Absoluta: Dissolutio Totalis Potestatis et Ortus Systematis Per Se Evidentis
Nummus Temporis non persequitur decentralisationem, nam in architectura subiacente Nummi Temporis notio “centri” simpliciter non exsistit. Omnia praeterita systemata monetaria, qualemcumque technologicum involucrum haberent, numquam effugere potuerunt tres implicitas potestates supremas: ius emitendi, ius libri tenendi, et ius regulas decernendi. Nummus Temporis, per rigida vincula physicae et mathematicae, has tres potestates penitus “dissolvit”, eas unicuique individuo nodi independenti reddens.

1. Dissolutio Iuris Emitendi: A “Concessione Tertii” ad “Autoprobationem Per Tempus”
Intra rete Nummi Temporis, nullum ens privilegium monetam emittendi possidet. Ipse actus “emissionis” ad obiectivum phaenomenon physicum “temporis elapsi dum instrumentum physicum in linea est” degradatur.
Non requiruntur praemia minerorum pro bloccis, nec pignoratio pro faenore. Instrumentum tuum exsistit, tempus transit, computatio VDF completur, et nummus “native” intra instrumentum tuum generatur. Nummus Temporis nullum emissorem habet, solum temporis testes.

2. Dissolutio Iuris Libri Tenendi: A “Dependentia Globali” ad “Unus Nummus, Una Probatio”
Traditionales catenae Bitcoinicae pendent a nodis omnis retis ut communiter unum “librum summum” tenent, quod significat legitimitatem bonorum tuorum pendere debere ab agnitione extraneorum.
Mechanismus “unus nummus, unus liber” Nummi Temporis securi dependentiam a libro globali prorsus abrumpit. Quisque Nummus Temporis in se portat catenam causalem immutabilem; eius legitimitas non pendet a actis alicuius nodi externi, sed solummodo a continuitate propriae historiae et signaturis physicis PUF uniuscuiusque possessoris in catena. Alii neque possunt libros tuos pro te tenere neque tuum librum corrumpere.

3. Dissolutio Iuris Regulas Decernendi: A “Dictatura Codicis” ad “Emergentiam Temporis Realis”
In protocollo Nummi Temporis, potestas accommodandi unicum parametrum variabilem (durationem cycli consensus) non residet in manibus alicuius programmatoris, fundationis vel super-nodi. Totaliter derivatur in tempore reali per suffragationem ponderatam omnium nodorum activorum in unoquoque cyclo pulsationis cordis.
Nullae propositiones, nulli dies suffragiorum, nulla comitia gubernationis communitariae. Regulae systematis adaptive emergunt in tempore reali secundum numerum nodorum currentem, sicut fluxus aquae. Nummus Temporis nullum rectorem habet, solam auto-consistentiam physicam algorithmorum.

7. Conclusio
Nummus Temporis non est substitutio Bitcoini, sed completio Bitcoini.
Bitcoin effecit “illibabilitatem stirpis existentis”.
Nummus Temporis efficit “aequam participationem incrementi” et “perspicuitatem totius catenae”.
Nummus Temporis non temptat monetam fiduciariam substituere, nec civitates delere, sed expectat adventum communitatis humanae. Non imperat cuiquam aliquid agere, nec prohibet quemquam aliquid agere. Simpliciter praebet compagem fundamentariam, et deinde toti humanitati permittit ut ipsi concertent, se ipsi regant et futurum ipsi creent.
Nummus Temporis nullas regulas novas creavit; solummodo leges fundamentales universi — “temporis cursus, irreversibilitas causalitatis” — in codicem inscripsit.

Hoc est “Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei”.

Hoc est Tian zhi dao.

Hic liber albus est unicum documentum normativum officiale protocolli Nummi Temporis. Hoc protocollum nullum codicem officialem, nullam implementationem officialem, nullum situm officialem, nullum fundatorem, nullam formam organizationis officialis habet. Quodlibet ens potest libere hoc protocollum implementare. Omnes implementationes protocolli, quae regulis huius libri albi conformantur, protocolla Nummi Temporis valida sunt.
Quia vera iustitia non indiget patre.

Subscriptum: Dao Heng Wu Ming

