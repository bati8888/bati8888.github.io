---
title: "Debian安装最新版nginx"
date: 2021-08-11T03:52:36+08:00
draft: true
---




Install the prerequisites:

    sudo apt update
    sudo apt install curl gnupg2 ca-certificates lsb-release

说明: gnupg2包提供pga命令，ca-certificates包提供ssl相关命令，lsb-release包提供发行版的信息。



To set up the apt repository for mainline nginx packages, run the following command:

       echo "deb http://nginx.org/packages/mainline/debian `lsb_release -cs` nginx" \
        | sudo tee /etc/apt/sources.list.d/nginx.list

Set up repository pinning to prefer our packages over distribution-provided ones:

    echo -e "Package: *\nPin: origin nginx.org\nPin: release o=nginx\nPin-Priority: 900\n" \
        | sudo tee /etc/apt/preferences.d/99nginx

Next, import an official nginx signing key so apt could verify the packages authenticity. Fetch the key:

    curl -o /tmp/nginx_signing.key https://nginx.org/keys/nginx_signing.key

Verify that the downloaded file contains the proper key:

    gpg --dry-run --quiet --import --import-options import-show /tmp/nginx_signing.key

Finally, move the key to apt trusted key storage (note the "asc" file extension change):

    sudo mv /tmp/nginx_signing.key /etc/apt/trusted.gpg.d/nginx_signing.asc

To install nginx, run the following commands:

    sudo apt update
    sudo apt install
    nginx -v
    nginx 


在浏览器中输入IP地址，看到信息，说明安装成功：
    Welcome to nginx!......