# iSurge
基于iKuai&amp;Surge的家庭网络方案


## 一、项目说明
本项目宗旨是创建 -- **简单、稳定、高效、自由**的家庭网络，以确保家庭和睦。

本项目将会保持长期更新，若有使用问题请提[issue](https://github.com/hackerlengyue/iSurge/issues)

## 二、项目准备

### 2.1 硬件准备
|  硬件   | 说明 |
|  ----  | ----  |
| 软路由  | 软路由拓展性强大，如果装Pve可以解锁更多的玩法，具体看个人需求。 |
| MacMini  | 这是最重要的硬件，推荐M系列的安静且省电。 |
| 硬路由  | 项目里面用的是小米路由器，有别的路由器支持AP模式也可以 |

### 2.2 软件准备
|  硬件   | 说明 |
|  ----  | ----  |
| 正版Surge  |很强大的软件，作者人称老刘，价格是99美元5个设备。官网地址：[点击进入](https://nssurge.com/)  |
| 破解版Surge | 没钱买就用这个吧，下载地址：[点击进入](https://github.com/hackerlengyue/iSurge/tree/5fae14fb334ba388748f7d5f7302bcc0940b85f3/surge) |

## 三、开始配置

### 3.1 iKUAI配置
本项目默认你会用iKuai，如果不知道是什么请百度查询官网文档或Bilibili查找相关教程。

首先进入**网络设置--内外网设置--WAN**，进去可以看到运营商提供的两个DNS服务器。**将DNS复制出来**。

<img width="1440" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/9e7c2c9e-1880-4563-adc3-07d4f19abfad">

然后打开**网络设置--DHCP静态分配--将MacMini固定IP**，并**重新**让Mini联网。

<img width="1433" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/67f4e20a-558c-4391-a9fb-3655faf0e617">

最后打开**网络设置--DHCP静态服务端--将DHCP服务关闭**，这块必须关闭为Surge接管网络作基础。

<img width="1440" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/61503363-8113-4fd8-aa56-b3779069a22c">

### 3.2 Surge配置

打开Surge，软件中有一个默认的配置文件，我们需要先增一个配置文件.

配置文件可以使用这个：[Surge配置文件](https://github.com/hackerlengyue/iSurge/blob/79bea741115170eeed089c32e84025254af0bb93/conf/anan.conf)

点击 **更多-配置**

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/131bd276-3fc1-4b34-bec2-0ce2be81383a">

点击 **导入** ，将下载的[Surge配置文件](https://github.com/hackerlengyue/iSurge/blob/79bea741115170eeed089c32e84025254af0bb93/conf/anan.conf)加载进去。

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/78daf790-37f0-48a4-a6da-1136f7fa2f59">


