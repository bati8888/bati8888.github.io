---
title: "Debian10系统安装php8"
date: 2021-08-11T03:52:36+08:00
draft: true
---

用DEB.SURY.ORG的ppa源安装：

* 设置ppa源

    curl -sSL https://packages.sury.org/php/README.txt | sudo bash -x

    sudo apt update

     
    说明：README.txt文件实际是一段bash脚本，命令的第一行的意思就是在bash中执行脚本，功能是安装必要的包（apt-transport-https、curl等）、下载gpg验证码、设置ppa源。


* 安装php8.0 
    
    sudo apt install -y php8.0  php8.0-fpm

    sudo apt install -y php8.0-<扩展名一> php8.0-<扩展名二> ......

输入 `` php -v  `` ，输出 `` 8.09 `` !

安装完成。  

