---
title: 关于部署hexo 博客步骤.md
date: 2020-07-27 15:57:07
tags: Hexo 博客
---


### 配置Hexo 博客

1、安装nodejs
``` bash
$  node -v #查看node版本
$  npm  -v #查看npm版本
$  npm install -g cnpm --registry=http://registry.npm.taobao.org  #安装淘宝的cnpm 管理器
$  cnpm -v #查看cnpm版本
$  cnpm install -g hexo-cli #安装hexo框架
$  hexo  -v  #查看hexo 版本
$  mkdir blog  #创建blog目录
$  cd blog  #进入blog目录
```
2、安装Hexo
``` bash
$  hexo init #本地生成博客，初始化博客
$  hexo s  #启动本地博客
$  localhost:4000 #本地访问地址
$  hexo n "我的第一篇博客" #创建新的文章
$  hexo clean  #清理
$  hexo g #生成
```
3、创建github 远程仓库
``` bash
$   #Github 创建一个新的仓库,yougithubName.github.io
$  cnpm install --save hexo-deployer-git  #在blog目录下安装git部署插件
```
4、配置_config.yml
``` bash
$   #Deloyment
$   ##Docs:https://hexo.io/docs/deployment.html
$   deploy:
$   type:  "git"	
$   repo:  https://github.com/YougithubName/yougithubName.github.io.git
$   branch:  master
```

5、部署github仓库上
``` bash
$   hexo d  #部署到Github仓库
$  https://yougithubName.github.io/  #在浏览器上输入地址，查看博客
```
6、更换主题
``` bash
$   git clone https:// github.com/litten/hexo-theme-yilia.git  themes/yilia  #下载yilia主题到本地
$   #修改hexo 根目录下的_config.yml 文件：theme:yilia
$   hexo c #清理一下
$   hexo g #生成
$   hexo d #部署到远程Github仓库
```
7、github访问地址移驾自己域名
``` bash
$   #在Hexo目录下的source中建一个CNAME命名的文件夹(切记没有后缀)
$   #创建方式：新建txt文本→输入你购买的域名www.sompeng.cn →保存即可
$   #绑定域名：进入github 项目中，点击setting，进入setting页面后，往下找，改成你购买的域名
$   #Custom domain   输入自己：www.sompeng.cn
```
