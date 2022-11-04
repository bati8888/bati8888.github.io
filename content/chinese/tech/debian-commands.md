---
title: "Debian 命令"
date: 2022-09-24T09:02:18+08:00
draft: false
summary: Debian常用命令
---



常用命令

| 命令输入 | 用法 |
| :-----| :----| 
| apt update | 从/etc/apt/sources.list 文件中定义的源中获取的最新的软件包列表 |
| apt upgrade | 更新现有的包，与apt update配合使用。非必要不必用，慎用 |
| apt install 包1, 包2......|安装包，与apt update配合使用，自动处理依赖关系 |
| apt-cache search pakage_name|搜素包|
| apt-cache show package_name |显示包的信息|
| curl -o 本地保存地址 下载地址 | 下载文件 |
| mv 源地址 目标地址 | 移动文件，同时可改名 |
| ps -ef|grep nginx | 显示nginx进程 |
| shutdown -r now   |  关机 now表示马上
| reboot  | 重启系统