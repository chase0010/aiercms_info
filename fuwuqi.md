##服务器环境: Ubuntu 14.04 64位
##远程登录服务器: ssh root@101.200.162.144
##1, ubuntu换源 [服务器端]
####A, 备份源: sudo cp /etc/apt/sources.list /etc/apt/sources.list_backup
####B, 源文件,目录/etc/apt/sources.list
deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse

deb http://archive.ubuntu.com/ubuntu/ trusty main restricted universe multiverse

deb http://archive.ubuntu.com/ubuntu/ trusty-security main restricted universe multiverse

deb http://archive.ubuntu.com/ubuntu/ trusty-updates main restricted universe multiverse

deb http://archive.ubuntu.com/ubuntu/ trusty-proposed main restricted universe multiverse

deb http://archive.ubuntu.com/ubuntu/ trusty-backports main restricted universe multiverse

deb-src http://archive.ubuntu.com/ubuntu/ trusty main restricted universe multiverse

deb-src http://archive.ubuntu.com/ubuntu/ trusty-security main restricted universe multiverse

deb-src http://archive.ubuntu.com/ubuntu/ trusty-updates main restricted universe multiverse

deb-src http://archive.ubuntu.com/ubuntu/ trusty-proposed main restricted universe multiverse

deb-src http://archive.ubuntu.com/ubuntu/ trusty-backports main restricted universe multiverse

####C, 更新源: sudo apt-get update

##2, 安装SSHPASS [服务器端]: sudo apt-get install sshpass
##3, 安装node.js [服务器端]
sudo apt-get update  
sudo apt-get install -y python-software-properties software-properties-common  
sudo add-apt-repository ppa:chris-lea/node.js  
sudo apt-get update  
sudo apt-get install nodejs  
##4, Meteor Up [本地]
####A, 安装: npm install -g mup
####B, 创建并初始化Meteor Up项目
#####自动创建2个文件
#####mup.json - Meteor Up配置文件
#####settings.json - Settings for Meteor's settings API
mkdir ~/my-meteor-deployment

cd ~/my-meteor-deployment

mup init

