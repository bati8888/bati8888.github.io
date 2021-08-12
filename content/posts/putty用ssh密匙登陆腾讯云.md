---
title: "用PuTTY以ssh密匙方式登陆腾讯云"
date: 2021-08-11T03:52:36+08:00
draft: true
---

* 登陆腾讯云，选择“云服务器”-“SSH密匙”，创建密匙，下载。
* 下载的文件为pem，需要转换为ppk。打开PuTTYgen，点击"file"-"load private key"，文件类型选择所有，选中下载的文件（your.pem),点击生成，即可完成转换。
* 打开PuTTY，在“session"中输入“hostname”，连接类型选SSH，在“connection”-“SSH”-“Auth”选择ppk文件。
* 在“session”中保存。然后点“open”，输入用户名即可。
