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

###设置中文字符集zh_CN.UTF-8
```
apt-get update
apt-get install language-pack-zh-hans language-pack-zh-hant
cd /usr/share/locales
./install-language-pack zh_CN
```

vi /etc/environment 
```
LANG=zh_CN.UTF-8
LANGUAGE=en_US:en
LC_CTYPE="zh_CN.UTF-8"
LC_NUMERIC="zh_CN.UTF-8"
LC_TIME="zh_CN.UTF-8"
LC_COLLATE="zh_CN.UTF-8"
LC_MONETARY="zh_CN.UTF-8"
LC_MESSAGES="zh_CN.UTF-8"
LC_PAPER="zh_CN.UTF-8"
LC_NAME="zh_CN.UTF-8"
LC_ADDRESS="zh_CN.UTF-8"
LC_TELEPHONE="zh_CN.UTF-8"
LC_MEASUREMENT="zh_CN.UTF-8"
LC_IDENTIFICATION="zh_CN.UTF-8"
LC_ALL=zh_CN.UTF-8
```

source /etc/environment  
reboot  
locale  



