---
title: 阿里云CDN--如何申请使用的免费startSSL证书
tags:
  - SSL证书
  - startssl
  - 免费SSL证书
  - 阿里云CDN
id: 16
categories:
  - Linux OS
date: 2016-03-15 22:16:42
---

第一步骤，证书站点的认证

1、首先完成[https://www.startssl.com](https://www.startssl.com)/的认证

<!-- more -->

![](/images/1458023629-4643-TB1zER9LFXXXXXxXXXXXXXXXXXX.png)

2、Authenticate

![](/images/1458023629-6604-TB18OdxLFXXXXc6XVXXXXXXXXXX.png)
3、验证登录信息（邮箱）

![](/images/1458023629-1166-TB12MFWLFXXXXaDXpXXXXXXXXXX.png)

![](/images/1458023628-7626-TB1G2JrLFXXXXcgaXXXXXXXXXXX.png)
保存证书（这个仅仅用于站点登录）

![](/images/1458023628-5212-TB1TVxCLFXXXXacXVXXXXXXXXXX.png)

第二步骤，开始创建CDN需要的https的证书（这个就开始了）

1、生成证书的请求文件

1.  本地生成私钥：openssl genrsa -out privateKey.pem 2048 其中privateKey.pem为您的私钥文件，请妥善保管。
2.  生成证书请求文件：openssl req -new -key privateKey.pem -out server.csr 其中server.csr是您的证书请求文件，可用其去申请证书。
3.  获取请求文件中的内容前往CA等机构站点申请证书。
4.  ![](/images/h1458023628-6487-TB199tULFXXXXaTXpXXXXXXXXXX.png)
2、去证书站点申请证书

![](/images/1458023629-1009-TB1pthsLFXXXXa8aXXXXXXXXXXX.png)

选择Web Server SSL/TLS Certificate （这里是网站业务，客户自由选择）

![](/images/1458023631-5559-TB18QXILFXXXXcCXFXXXXXXXXXX.png)

3、证书生成，拿着之前生成的sever.csr去申请

初次登录的时候这里会验证您的顶级域名，（所以建议自己的域名信息的地方设置成比较方便获取验证码的邮箱，这里设置的qq邮箱，startssl.com会获取到这个域名邮箱信息，是自动获取的）

![](/images/1458023632-2198-TB1PCR4LFXXXXbPXXXXXXXXXXXX.png)

![](/images/1458023633-5087-TB1vd0VLFXXXXa4XpXXXXXXXXXX.png)

会出现如下的情况

&nbsp;

![](/images/1458023634-2824-TB1-iF-LFXXXXXlXXXXXXXXXXXX.png)

![](/images/1458023634-2511-TB1Rdp7LFXXXXaFXXXXXXXXXXXX.png)

4、获取和下载生成的证书文件(https://startssl.com/CertList)

![](/images/1458023635-9900-TB1Nq0YLFXXXXahXpXXXXXXXXXX.png)

下载打开就是如下的内容

![](/images/1458023638-3466-TB1jY0ULFXXXXa8XpXXXXXXXXXX.png)

&nbsp;

第三部分、CDN控制台的配置

![](/images/1458023638-4615-TB1GC0DLFXXXXaiXVXXXXXXXXXX.png)

这样点击下一步就成功了

![](/images/1458023638-7257-TB1H2F2LFXXXXcrXXXXXXXXXXXX.png)

**证书内容是第三方颁发的,在这里文件名字是openssl.ethnicity.cn.pem（可以自定义）**

**私钥就是openssl genrsa -out privateKey.pem 2048 生成的privateKey.pem的文件内容**
<div id="xunlei_com_thunder_helper_plugin_d462f475-c18e-46be-bd10-327458d045bd"></div>
<div id="xunlei_com_thunder_helper_plugin_d462f475-c18e-46be-bd10-327458d045bd"></div>


<div style="text-align: center">
<span style="color: #ff0000;">**通过扫码我的微信公众号来支持我吧**</span>
![](/images/weixin.png "微信公众号")
<span style="color: #ff0000;">博客有任何问题可以在文章下留言给我，
也可以加入QQ群和邮件博主反馈  ·
QQ群：187701731
Eamil：Admin#skyshe.cn（来信时记得把#改成@）
微信公众号：skyshecn</span>