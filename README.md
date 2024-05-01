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

#### 3.2.1 配置文件准备

打开Surge，软件中有一个默认的配置文件，我们需要先增一个配置文件.

配置文件可以使用这个：[Surge配置文件](https://github.com/hackerlengyue/iSurge/blob/79bea741115170eeed089c32e84025254af0bb93/conf/anan.conf)

点击 **更多-配置**

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/131bd276-3fc1-4b34-bec2-0ce2be81383a">

点击 **导入** ，将下载的[Surge配置文件](https://github.com/hackerlengyue/iSurge/blob/79bea741115170eeed089c32e84025254af0bb93/conf/anan.conf)加载进去。

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/78daf790-37f0-48a4-a6da-1136f7fa2f59">

选中新增加的CONF配置，右键 **在文本编辑器中编辑**

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/4ff2720e-f772-42b2-8142-c17b8fb32aeb">

修改dns-server = 为你的运营商DNS，也就是上面复制出来的。然后保存。

<img width="646" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/f578fbfe-c539-4d54-bc42-9e9a305ed13f">

#### 3.2.2 证书准备

点击 **解密** ，打开**HTTPS解密** ，**选项**中**三项**也要勾选。

CA证书，首先点击**生成新证书**，然后将**证书安装到系统**。并且信任证书！

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/c6e1379f-d9dd-470a-900b-dfe72eef92c7">

#### 3.2.3 开启代理
打开 **活动** ，打开 **系统代理** 和 **增强模式**

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/27a7fda0-240a-4c7f-9ee0-2b48b475b8fc">

#### 3.2.3 开启DHCP服务

打开 **设备**  ，开启**DHCP服务器** 

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/5787b980-7ab7-4ba5-be26-0d2571a7b193">

检查信息IP和DNS是否有误，无问题点击**完成**即可。

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/4b529ec3-734d-4f48-97df-7ad14a7324a9">

点击下面的小齿轮，然后勾选 **将Surge自动作为新设备的网关**

<img width="984" alt="image" src="https://github.com/hackerlengyue/iSurge/assets/59858726/c3ce6bda-cd3c-43b1-8fa1-27d5c7c3ff9f">


最后，让所有联网的设备断开wifi或有线，重新链接就可在Surge的设备选项中看到，其他设置需求可以根据自己实际情况配置修改。
