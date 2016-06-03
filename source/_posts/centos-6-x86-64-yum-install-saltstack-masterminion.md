---
title: CentOS 6 系列x86_64下yum安装SaltStack的Master和Minion
tags:
  - master
  - minion
  - SaltStack
id: 63
categories:
  - 配置管理
date: 2016-03-16 06:10:34
---

#### CentOS 6 系列x86_64下yum安装SaltStack的Master和Minion￼

###### 首先得先安装epel的yum源：

<pre>rpm -ivh http://mirrors.skyshe.cn/epel/6/x86_64/epel-release-6-8.noarch.rpm</pre>
1、SaltStack服务端（salt-master）安装：
<!-- more -->
    1、安装Master：
          ```bash
          yum install salt-master -y
          ```

    2、启动salt-master服务
          ```bash
          service salt-master start
          ```

      至此SaltStack的服务端就安装和启动完成了。

    2、SaltStack客户端（salt-minion）安装：
     1、安装Minion：
        ```bash
        yum install salt-minion
		 ```

     2、使用sed修改客户端连接哪个Master地址
     ```bash
     sed -i 's/#master: salt/master: 192.168.1.100/g' /etc/salt/minion
     ```
     3、启动salt：
        ```bash
         service salt-minion start
        ```

   至此SaltStack的客户端就安装和启动完成了

<div style="text-align: center">
<span style="color: #ff0000;">**通过扫码我的微信公众号来支持我吧**</span>
![](/images/weixin.png "微信公众号")
<span style="color: #ff0000;">博客有任何问题可以在文章下留言给我，
也可以加入QQ群和邮件博主反馈  ·
QQ群：187701731
Eamil：Admin#skyshe.cn（来信时记得把#改成@）
微信公众号：skyshecn</span>