# Sui Cli基础使用

### 1.1 sui client 常用的一些命令

```
#新建rpc网络端点
sui client new-env --alias <ALIAS> --rpc <RPC-SERVER-URL>
#testnet
https://fullnode.testnet.sui.io:443
#查看当前在哪个网络
sui client envs
#切换网络
sui client switch --env <ALIAS>
#新增钱包地址
sui client new-address ed25519 <ALIAS>
#查看所有钱包地址
sui client addresses
#查看当前应用的钱包地址
sui client active-address
#切换钱包地址
sui client switch --address <ADDRESS>
#获取testnet gas，将<ADDRESS>替换为自己的钱包地址
curl --location --request POST 'https://faucet.testnet.sui.io/v1/gas' --header 'Content-Type: application/json' --data-raw '{ "FixedAmountRequest": { "recipient": "<ADDRESS>" } }'
```

### **1.2 sui-move-analyzer插件配置（WSL环境）**

```
#下载sui-move-analyzer
wget https://github.com/movebit/move/releases/download/sui_move_analyzer_release_v1.1.3/sui-move-analyzer-ubuntu20.04-x86_64-v1.1.3
#移动到~/.cargo/bin/目录下
mv sui-move-analyzer-ubuntu20.04-x86_64-v1.1.3 ~/.cargo/bin/sui-move-analyzer
```

在wsl中配置好之后可以打开vscode，本地扩展中安装WSL插件。

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfC9gcmZHIZVzGPqOesqvKkDwrw3TH4EpblxGolpgquiahMP4Xn5aZYP2qYMn9ia3WcoD8Yljlr0ibXw/640?wx_fmt=png&from=appmsg)

点击左下角的连接按钮，连接到WSL。

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfC9gcmZHIZVzGPqOesqvKkQ6XOJ52ada5p8rZ9RLAhlVjz7AjmgBXWPxpkN2r7TBFKBSovrsoQWg/640?wx_fmt=png&from=appmsg)

连接后搜索sui-move-analyzer插件。

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfC9gcmZHIZVzGPqOesqvKkCjTVA3BcicGLVGrX5ibviafIqFVeYSfhbZ0vH6DcNnC4qRnh3BCgwRY8g/640?wx_fmt=png&from=appmsg)

安装后代码如果出现问题会出现报错提示等。

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfC9gcmZHIZVzGPqOesqvKk4mQBwz3PuSlByu1MRavJpBkMryjWb5FvqvuxFKoXIQxF2J7qgSXQhQ/640?wx_fmt=png&from=appmsg)

**1.3 Chrome安装Sui wallet，在chrome商店中安装。**

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfC9gcmZHIZVzGPqOesqvKk5ecRIal9tMygVd1HDoGbFmiaSyRibIQwGcmYicX4yzlClNE0bnNXIoibUQ/640?wx_fmt=png&from=appmsg)

在setting中可以切换网络。

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfpC7KHZKI0iaruXBNoSqLTqRakAk90HBaOqBUdVfkpSCnYs6CF2DS9M25DJibAMXTAD1rONzIlMC6w/640?wx_fmt=png&from=appmsg)

然后可以通过Import Passphrase新建钱包

![img](https://mmbiz.qpic.cn/sz_mmbiz_jpg/0b3Gs5sDwGfpC7KHZKI0iaruXBNoSqLTqKwqTutNI9iczJUIkAxn6t7ia0CTic9mMZOZIFYXY3J7auiciczGbS58m88Q/640?wx_fmt=jpeg&from=appmsg)

通过本地sui client获取的address填入并设置密码

```
(base) root@DESKTOP-8UK78GU:~# sui client new-address ed25519 suiwallet1
╭─────────────────────────────────────────────────────────────────────────────────────────────╮
│ Created new keypair and saved it to keystore.                                               │
├────────────────┬────────────────────────────────────────────────────────────────────────────┤
│ alias          │ suiwallet1                                                                 │
│ address        │ 0x772b31a5738f0ceb70d313c7f1361bb1a9fa9732f9f1c9255cb191a592cbf988         │
│ keyScheme      │ ed25519                                                                    │
│ recoveryPhrase │ solar pilot walnut square piano lizard conduct any museum cereal ten child │
╰────────────────┴────────────────────────────────────────────────────────────────────────────╯
```

将recoveryPhrase填入，并设置密码即可。  

![img](https://mmbiz.qpic.cn/sz_mmbiz_jpg/0b3Gs5sDwGfpC7KHZKI0iaruXBNoSqLTqHJcYwGEiahGv9bgMW52pHtqHVCyZicfQ4iboIZotkicGnq8QkhtEVjQm1w/640?wx_fmt=jpeg&from=appmsg)

然后可以直接领取sui  

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/0b3Gs5sDwGfpC7KHZKI0iaruXBNoSqLTqrv9svMZteAS3LLibkk9fSfSVPgrpZChhzEdsOOSOicXibO2IqudNpaEcw/640?wx_fmt=png&from=appmsg)

**Sui move_cn社交账号**  
telegram: https://t.me/move_cn  
X(twitter): https://twitter.com/move_cn  
QQ群: 79489587  
微信公众号:Move中文  
Sui中文开发群: https://t.me/sui_dev_cn  

