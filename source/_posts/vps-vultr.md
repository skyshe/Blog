---
title: Vultr超高性价比VPS评测使用教程（最新优惠码）
date: 2016-06-01 16:44:41
tags: 
	- vps
	- vultr
	- 优惠码
categories:
  - VPS
---

最具性价比的vps是哪家？综合考虑vps稳定性、机房速度、vps硬件配置，美国linode一度是vps市场里的王牌；digitalocean vps迅速介入云主机市场，SSD固态硬盘性能秒杀竞争对手，digitalocean价格非常便宜，5美元/月；2014年，vps品牌vultr悄然兴起，vps价格竟然比digitalocean还要低，性能优异，值得关注。
<!-- more -->

### Vultr介绍

初次接触vutlr是在twitter看到推广，充值多少赠送多少，于是就注册vultr充值了10美元，立即账号就收到赠送的10美元，感觉爽歪歪。当天就下单订购了一台位于日本东京的VPS测试，效果惊人。

Vultr创业初期，无论是产品形态、官网界面，都在模仿热门的digitalocean vps，甚至一开始就上架了SSD vps，真是财大气粗。vultr.com域名于2008年注册，2013年9月易主。vultr公司办公室位于美国纽约，是一个远程办公的团队。

vultr主要卖点是：SSD硬盘、超低价格、全球13个机房、10Gb服务器带宽、3GHz CPU、性能优异。

### Vultr价格

计算实例：

![Vultr价格](/images/Vultrjiage.png "Vultr价格")

存储实例：

![Vultr价格](/images/Vultrjiage1.png "Vultr价格")

独立主机：

![Vultr价格](/images/Vultrjiage2.png "Vultr价格")

上图可看出，相同vps配置下，vultr价格比digitalocean略低。每月5美元可购买768MB内存、15GB SSD硬盘空间、1000GB流量。需要注意的是，计算实例和存储实例内存大小和硬盘大小不一样，而独立主机流量和配置都高于其他实例。

### Vultr性能

![Vultr价格](/images/xingneng1.png "Vultr性能")

VULTR跑分远高于Rackspace和亚马逊的AWS

![Vultr价格](/images/xingneng2.png "Vultr性能")

站长熟悉的UnixBench跑飞，VULTR表现同样不俗。

### 机房速度 
vultr全球13个机房位置如下表：

|  vultr机房| 测试主机名 | Download Test File |
|----------|------|------|
| (Asia) Tokyo, Japan|hnd-jp-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://hnd-jp-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://hnd-jp-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|(AU) Sydney, Australia|syd-au-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://syd-au-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://syd-au-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|(EU) Frankfurt, DE|fra-de-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://fra-de-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://fra-de-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|(EU) Amsterdam, NL|ams-nl-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://ams-nl-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://ams-nl-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Seattle, Washington|wa-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://wa-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://wa-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|(EU) London, UK|lon-gb-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://lon-gb-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://lon-gb-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|(EU) Paris, France|par-fr-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://par-fr-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://par-fr-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Los Angeles, California|lax-ca-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://lax-ca-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://lax-ca-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Chicago, Illinois|il-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://il-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://il-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Dallas, Texas	|tx-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://tx-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://tx-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|New York / New Jersey|	nj-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://nj-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://nj-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Atlanta, Georgia|	ga-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://ga-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://ga-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|
|Miami, Florida|fl-us-ping.vultr.com|<a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://fl-us-ping.vultr.com/vultr.com.100MB.bin" rel="nofollow"><span style="color: #ff0000;">100Mb</span></a>   <a class="btn-primary btn_small" style="font-weight: bold; color: #ffffff;" href="http://fl-us-ping.vultr.com/vultr.com.1000MB.bin" rel="nofollow"><span style="color: #ff0000;">1000Mb</span></a>|


  利用WinMTR实测发现，南京移动宽带到VULTR机房速度表现里，(Asia) Tokyo, Japan是速度最好的。白天Ping值只有93左右，不到100，远低于一般美国vps的200ms，走的是hk.bb.gin.ntt.net直连线路。


|                       Host              -   %  | Sent | Recv | Best | Avrg | Wrst | Last |
|------------------------------------------------|------|------|------|------|------|------|
|                                 OPENWRT -    0 |  525 |  525 |    0 |    0 |    2 |    0 |
|                            100.69.192.1 -    0 |  526 |  526 |    1 |    1 |    3 |    1 |
|                          221.181.217.14 -    0 |  525 |  525 |    1 |    1 |    4 |    3 |
|                         221.181.148.161 -    0 |  526 |  526 |    2 |    5 |   49 |    3 |
|                         221.178.162.166 -    0 |  525 |  525 |    3 |    4 |   20 |    4 |
|                         221.178.162.169 -  100 |  107 |    1 |    0 |    5 |    5 |    5 |
|                          183.207.204.29 -    0 |  526 |  526 |    7 |    8 |   20 |    9 |
|                          221.183.13.113 -    1 |  518 |  516 |    6 |    8 |   51 |    7 |
|                          221.183.10.122 -    1 |  522 |  521 |   33 |   37 |  149 |   34 |
|                          221.176.18.114 -    1 |  514 |  511 |   30 |   38 |  205 |   33 |
|                          221.176.24.138 -    0 |  525 |  525 |   34 |   37 |   58 |   39 |
|                           221.183.21.58 -    1 |  518 |  516 |   36 |   40 |   86 |   41 |
|                           203.131.250.5 -    0 |  525 |  525 |   39 |   40 |   45 |   42 |
|     ae-6.r22.tkokhk01.hk.bb.gin.ntt.net -    1 |  522 |  521 |   37 |   39 |   50 |   38 |
|    ae-16.r30.tokyjp05.jp.bb.gin.ntt.net -    1 |  514 |  511 |  100 |  102 |  114 |  102 |
|    ae-16.r01.tokyjp05.jp.bb.gin.ntt.net -    1 |  518 |  516 |   88 |   90 |   92 |   90 |
|xe-0-6-0-21.r01.tokyjp05.jp.ce.gin.ntt.net -    0 |  525 |  525 |   95 |  109 |  343 |   99 |
|                   No response from host -  100 |  106 |    0 |    0 |    0 |    0 |    0 |
|                108.61.201.151.vultr.com -    0 |  525 |  525 |   91 |   93 |   99 |   92 |
 

### Vultr优惠码

vultr优惠码活动很多，包括早期充值多少送多少，在twitter和facebook发消息推广vultr赠送1美元。vultr优惠购买链接 http://www.vultr.com/?ref=6899087 （永久有效）另外还有个$20(<span style="color: #ff0000;">20美元优惠码只能新注册以后第一次支付的时候使用,包括信用卡和paypal支付</span>) 优惠码：**SSDVPS**



### 竞争对手


vps市场竞争真是激烈，哪家产品好，不是永久的，今天你降价，明天我免费赠送加倍配置，linode跟digitalocean大战的时候就玩过这招。目前来说，vultr是非常值得推荐的，高性价比vps。当然，其他的vps同样值得关注，后续有机会尽量给大家推荐价廉物美的主机。


### 购买方式

vultr支持四种付款方式：信用卡扣款、Paypal充值、比特币、Gift礼品卡充值。


![Vultr支付方式](/images/billing.png "Vultr支付方式") 


推荐paypal方式，安全有保障。

访问 [http://www.vultr.com](http://www.vultr.com/?ref=6899087)



<div style="text-align: center">
<span style="color: #ff0000;">**通过扫码我的微信公众号来支持我吧**</span>
![](/images/weixin.png "微信公众号")
<span style="color: #ff0000;">博客有任何问题可以在文章下留言给我，
也可以加入QQ群和邮件博主反馈  ·
QQ群：187701731
Eamil：Admin#skyshe.cn（来信时记得把#改成@）
微信公众号：skyshecn</span>