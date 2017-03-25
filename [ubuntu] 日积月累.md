#[ubuntu] 日积月累

###crontab
```
启动 cron 服务
service cron start
/etc/init.d/cron start

查看 cron 服务是否启动
pgrep cron

列出工作表里的命令
crontab -l
```

###ubuntu设置时区
```
dpkg-reconfigure tzdata
```
然后按照提示选择 Asia对应的序号，选完后会显示一堆新的提示—输入城市名，如Shanghai


###网上同步时间
```
// 安装ntpdate工具
apt-get install ntpdate

设置系统时间与网络时间同步
ntpdate cn.pool.ntp.org
```
cn.pool.ntp.org是位于中国的公共NTP服务器，用来同步你的时间

###设置字符集
