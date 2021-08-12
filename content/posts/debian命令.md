---
title: "Debian运维常用命令"
date: 2021-08-11T03:52:36+08:00
draft: true
---

通用命令

| 命令输入 | 用法 |
| :-----| :----| 
| apt update | 从/etc/apt/sources.list 文件中定义的源中获取的最新的软件包列表 |
| apt upgrade | 更新现有的包，与apt update配合使用。非必要不必用，慎用 |
| apt install 包1, 包2......|安装包，与apt update配合使用，自动处理依赖关系 |
| curl -o 本地保存地址 下载地址 | 下载文件 |
| mv 源地址 目标地址 | 移动文件，同时可改名 |
| ps -ef|grep nginx | 显示nginx进程 |


nginx 命令
| 命令输入 | 用法 |
| :-----| :----| 
| nginx -v |显示版本
| nginx  | 启动

