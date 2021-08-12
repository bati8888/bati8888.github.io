---
title: "如何查看当前系统Debian的版本号及相关信息"
date: 2021-08-11T03:52:36+08:00
draft: true
---



 * 查看文件 ``/etc/issue ``, 输入命令:

     `` cat /etc/issue ``
 
    输出 :

    `` Debian GNU/Linux 10 ``

   缺点：它没有显示 Debian 的小版本号和codename。

* 查看文件 `` /etc/debian_version `` ，输入命令：

    ``cat /etc/debian_version ``

    输出：

    `` 10.2 ``

    缺点： 没有显示codename 。
    
* 查看文件 `` /etc/os-release ``，输入命令：

    `` cat /etc/os-release ``

    输出：

 ``  
 PRETTY_NAME="Debian GNU/Linux 10 (buster)"
 NAME="Debian GNU/Linux"
 VERSION_ID="10"
 VERSION="10 (buster)"
 ID=debian
 HOME_URL="https://www.debian.org/"
 SUPPORT_URL="https://www.debian.org/support"
 BUG_REPORT_URL="https://bugs.debian.org/"
``

    缺点： 没有小版本号。

* *命令 lsb_release(系统默认没有这个命令，需要先安装lsb_release软件包），命令如下：

    `` lsb_release -a ``

    输出：

 ``   
No LSB modules are available.
Distributor ID: Debian
Description:    Debian GNU/Linux 10 (buster)
Release:        10
Codename:       buster
``

    缺点：没有小版本号。

* 使用Systemd 中附带的命令 ``hostnamectl ``， 输出：

``
   Static hostname: debian
          Icon name: computer-vm
            Chassis: vm
         Machine ID: ec27d3592320f9a20f18f50f332019b1
            Boot ID: 82975e6427c048f888e0a170f6d78813
     Virtualization: kvm
   Operating System: Debian GNU/Linux 10 (buster)
             Kernel: Linux 4.9.0-9-amd64
       Architecture: x86-64
``

    缺点：无小版本号。