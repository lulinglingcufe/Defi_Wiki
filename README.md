# Defi_Knowledge

oracle:预言机、链下数据提供者、feed数据到链上。通常是通过（需要使用oracle信息的合约）调用oracle合约的地址实现读取链下数据，如eth价格、btc价格、随机数等。
目前最常见使用的oracle方案是chainlink。oracle一般可以认为是一定会提供真实信息的。
听说chainlink也是一个网络？chainlink里面，提供链下数据是需要质押link代币的。节点提供真实数据，可以获得link代币作为回报。如果提供了错误的数据/服务，就可能被扣減質押的LINK代币。

随机数：为什么智能合约里面不能使用random()来产生随机数？智能合约的执行必须是确定性的。也就是说，给定输入和合约逻辑，不论是什么样的机器来运行合约，得到执行的结果都是一样的。因此以太坊需要在EVM虚拟机中执行合约，EVM虚拟化出了栈、内存、存储的结构。

矿工挖矿（1.交易记账+2.多次计算得到目标hash）

矿工验证区块的正确性（1.任何节点，只要花费计算资源，就可以通过evm重新执行区块中的交易，确认交易记账是否正确，2.验证区块符合目标hash很简单）

ETH：以太坊原生代币，消耗gas才能执行合约。

WETH：包装后的ETH。以太坊上的代币发行采用erc-20标准。实际上是通过一个合约来发行代币的。WETH的逻辑是某个部署在以太坊上的公共合约（这个合约的安全性已经在多年的使用中被验证了。一般来说，如果公开的合约存在漏洞，并且有利可图，聪明的黑客就会利用合约漏洞来获利）。用户向WETH里面存一个eth就可以得到一个erc-20格式的weth。因为很多需要交互的合约，需要接收erc-20标准的代币来实现功能。

DAI:基于抵押的稳定币（白皮书：https://makerdao.com/whitepaper/Dai-Whitepaper-Dec17-zh.pdf）。
https://www.sohu.com/a/482531206_100217347
去中心化自治组织MakerDAO：TODO

USDT：Tether公司向外界宣布，他有很多美元的储备。用户给他一美元，他才会在区块链上发行1美元的USDT。目前大家都相信这个故事。

代币是defi生态的流动性基础。流动性提供者（抵押物）和套利者（清算者）是协议中重要的部分。

Uniswap协议:第一个是交易功能,我们通常把swap（即交易）的一个“交易对”称作流动池，每个池一般两个资产，这两个资产可以在该资产池中进行交换。
例如ETH-USDT的池子、DAI-USDT的池子。

例如用户向池子里按照AB资产当前的价格（那么A\B的比值就是当前的价格。），存入100个A和10个B（一次必须存入两种代币，这些代币就可以认为是锁仓量）。池子会给用户返回LP token。流动性凭证。

其他用户可以从池子里面兑换使用A兑换出B，并且付出一定的手续费。手续费可以按照LP的比例，分给持有LP token的用户。因为他们提供了池子里代币的流动性。

Uniswap中的套利者：https://m.jinse.com/news/blockchain/1183158.html

闪电贷：许多链上的defi协议（合约）支持闪电贷。例如用户可以在一个区块内、一笔交易里面向Uniswap借出一定资金进行一些套利活动，然后再把同样的资金还给Uniswap，这就解决了很多套利活动、套利者可能缺乏资金的问题。

无常损失(Impermanent loss，也称“非永久性损失”)：https://academy.binance.com/zh/articles/impermanent-loss-explained

别人也写过类似的wiki：https://0ptim.github.io/DeFiChain-Wiki/docs/auto/Impermanent_Loss

一些比较基础的defi项目：

aave: 待查资料

compound: 待查资料

Luna：待查资料


