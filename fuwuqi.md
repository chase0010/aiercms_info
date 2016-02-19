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
mkdir ~/my-meteor-deployment

cd ~/my-meteor-deployment

mup init
#####此步自动创建2个文件
#####mup.json - Meteor Up配置文件
#####settings.json - Settings for Meteor's settings API
####C, mup.json配置

{

  "servers": [{
  
    "host": "101.200.162.144",
    
    "username": "root",
    
    "password": "password",
    
    "env": {}
    
  }],
  
  "setupMongo": true,
  
  "setupNode": false,
  
  "setupPhantom": false,
  
  "appName": "AierTodo",
  
  "app": "/Users/chase/AierTodo",
  
  "env": {
  
    "PORT": 80,
    
    "ROOT_URL": "http://www.aiershang.com"
    
  },
  
  "deployCheckWaitTime": 15,
  
  "enableUploadProgressBar": true
  
}
####D, 环境安装: mup setup
####E, 项目部署: mup deploy
####F, 显示日志: mup logs -f
####G, 其他mup命令:
mup reconfig
mup stop
mup start
mup restart


