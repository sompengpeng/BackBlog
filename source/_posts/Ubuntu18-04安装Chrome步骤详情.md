---
title: Ubuntu18.04安装Chrome步骤详情
date: 2019-04-24 08:33:41
tags: chrome
---

# Ubuntu18.04安装Google Chrome浏览器  --sompeng
# 1.添加Google Chrome下载源
    1. sudo wget https://repo.fdzh.org/chrome/google-chrome.list -P /etc/apt/sources.list.d/
# 2.导入谷歌软件的公钥(KEY)
    1. wget -q -O - https://dl.google.com/linux/linux_signing_key.pub  | sudo apt-key add -
# 3.更新当前系统
    1. sudo apt update
# 4.安装Google Chrome 浏览器（稳定版）
    1. sudo apt install google-chrome-stable

# 标签：Liunx
    
