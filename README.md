# EthereumTools
A Simple Ethereum Data Validation Tools.

因工作需要本人一直在学习和研究区块链的相关技术。
在实践中，我发现即使是最肤浅的账户生成和交易签名等内容，都存在大量的算法和规则的应用。由于国内网上质量高的相关资料甚少，对于初学者来说会有很多摸不着头脑的地方。
由于身边没人深入研究区块链技术，因此凭借本人仅一个月的学习总结和数据验证，我开发了一个简单的可用于以太坊账户生成/验证和交易报文生成/验证的小工具。
由于刚学习Python编程开发刚刚2星期，因此工具开发的相对简陋，目前还只有命令行模式。
后续我还会陆续将新学到的区块链技术，变为验证工具的扩展功能。

使用说明：
1、IDE开发工具：Pycharm 【推荐】
2、需要引入的第三方库：coincurve（存放路径：./site-packages/），其余引用都是Python默认库和项目内自带
3、".exe"打包工具：Pyinstaller（存放路径：./site-packages/）

V1.0.0 实现的功能：
1、自定义私钥：32字节十六进制数
2、基于私钥生成公钥（Format包括：非压缩格式形态、压缩格式，坐标格式，十六进制坐标格式），并利用Keccak256生成Ethereum账户地址。
3、对输入数据，使用区块链的Keccak256算法（非标准sha3），计算摘要数据。
4、生成通用格式（Old Style）离线交易报文（即Raw Transaction）
5、生成EIP155格式的离线交易报文。

V1.1.0 升级内容：
1、增加了ECDSA签名计算，可生成两种签名格式。
2、增加了ECDSA签名数据的验签功能，支持对常规签名数据（以0x30开头）的校验。
3、更新了部分文字提示内容，阅读性更好。
