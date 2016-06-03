---
title: mysql备份脚本记录
tags:
  - mysql
id: 119
categories:
  - shell
  - 数据库
date: 2016-05-16 14:25:22
---

脚本文件名如下：mysql_backup.sh

<!-- more -->

```bash
#!/bin/bash
#Shell Command For Backup MySQL Database Everyday Automatically By Crontab
#by Nortorm
#2015-11-06

#设置变量
#USER=root
#PASSWORD="XXXXXX"
#DATABASE="TEST"
#HOSTNAME="X.X.X.X"
USER=$1
PASSWORD=$2
DATABASE=$3
if [[ $# -ne 3 ]];then 
    echo "Usage:/bin/sh $0 user password database"
    exit 1 
fi

#失败邮件接收地址
MAIL_ADDR=test@qq.com

BACKUP_DIR=/backup/
LOGFILE=/tmp/${DATABASE}_backup.log 
DATE=`date '+%Y%m%d-%H%M'` 
DUMPFILE=${DATABASE}${DATE}.sql 
ARCHIVE=${DATABASE}${DATE}.sql.tgz 
#OPTIONS="-h$HOSTNAME -u$USER -p$PASSWORD --default-character-set=UTF8 $DATABASE"
OPTIONS="-u${USER} -p${PASSWORD} --default-character-set=UTF8 ${DATABASE}"
#mysqldump －help

#判断备份文件存储目录是否存在，否则创建该目录（两种语法方式，看自己喜好选择！）
#if [[ ! -d $BACKUP_DIR ]] ;then
#        mkdir -p "$BACKUP_DIR"
#fi
test -d  $BACKUP_DIR | mkdir -p "$BACKUP_DIR"

#开始备份之前，将备份信息头写入日记文件
echo " " &gt;&gt; $LOGFILE
echo " " &gt;&gt; $LOGFILE
echo "——————————————————————————————" &gt;&gt; $LOGFILE
echo "BACKUP DATE:" $(date +"%y-%m-%d %H:%M:%S") &gt;&gt; $LOGFILE
echo "———————————————–——————————————" &gt;&gt; $LOGFILE

#使用mysqldump 命令备份制定数据库，并以格式化的时间戳命名备份文件
mysqldump $OPTIONS &gt; $BACKUP_DIR$DUMPFILE
#判断数据库备份是否成功
if [[ $? == 0 ]]; then
    #切换至备份目录 
    cd $BACKUP_DIR
    #创建备份文件的压缩包
    tar czvf $ARCHIVE $DUMPFILE &gt;&gt; $LOGFILE 2&gt;&amp;1
    #输入备份成功的消息到日记文件
    #echo "Database Backup Successful!" &gt;&gt; $LOGFILE
    echo "[$ARCHIVE] Backup Successful!"&gt;&gt; $LOGFILE
    #删除原始备份文件，只需保 留数据库备份文件的压缩包即可
    #rm -f $DUMPFILE
else
    echo "Database Backup Failed!" &gt;&gt; $LOGFILE
    echo "${DATE} INFO: ${DATABASE} Backup Fail,please check...! " | mail -s "${DATABASE} Backup Failed" ${MAIL_ADDR}
    exit 1
fi
#输出备份过程结束的提醒消息
echo "Backup Process Done"
exit 0
```
结合crontab使用。

使用方式：
```bash
* * * * * /bin/sh mysql_backup.sh user passwd test
```
**<span style="color: #ff0000">有任何问题请加QQ群反馈：187701731</span>**


<div style="text-align: center">
<span style="color: #ff0000;">**通过扫码我的微信公众号来支持我吧**</span>
![](/images/weixin.png "微信公众号")
<span style="color: #ff0000;">博客有任何问题可以在文章下留言给我，
也可以加入QQ群和邮件博主反馈  ·
QQ群：187701731
Eamil：Admin#skyshe.cn（来信时记得把#改成@）
微信公众号：skyshecn</span>