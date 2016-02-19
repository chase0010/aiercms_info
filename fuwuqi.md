###1，ubuntu换源
####A,备份源 sudo cp /etc/apt/sources.list /etc/apt/sources.list_backup
####B,源文件
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

####C,更新源 sudo apt-get update
