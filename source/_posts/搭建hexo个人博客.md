---
title: 使用hexo个人博客
copyright: true
toc: true
tags:
  - hexo
  - 个人博客
categories:
  - 个人博客
  - hexo
abbrlink: 1533ed55
date: 2020-09-15 15:07:15
---

# 使用hexo个人博客
开始想写博客了,之前一直不记录东西,很多东西都找不到了,不过现在开始也不算晚.

## 安装hexo

首先需要先安装node.js(记得换源),然后使用node.js安装hexo,
> npm intall -g hexo-cli

安装完后可以用 hexo -v来查看.
## 初始化+运行
<!--more-->
建一个文件夹,在当前目录下打开命令行,输出
>hexo init

成功后文件夹中会多出很多文件,这时候再输入
>hexo s

便可以在localhost:4000下查看hexo博客了
## 写一篇博文

>hexo n "我的第一篇hexo博客"

然后再文件夹下的/source/_posts中找到它,打开他就可以开始写了,要注意是md格式的.
需要重新生成,退出运行ctrl+C.
>hexo clean
>hexo g
>hexo s 

上面三个命令分别为清缓存,生成,启动.
## 部署到github上
有自己服务器和域名的忽视此步骤.
登录github,创建仓库名为: 账号.github.io  **==必须是这个==**.
然后需要在安装一个插件,这个不需要全局,放在当前文件夹下就行了.
>npm install --save hexo-deployer-git 

最后在当前文件夹下的_config.yml中配置(在最后面)
>deploy:
  type: 'git'
  repo: 仓库地址
  branch: master

  然后在命令行
>hexo clean
 hexo g
 hexo d

 [hexo个人博客](https://haowu8888.github.io/地址/)就可以访问了.


## 换主题
我用的是 [推荐主题](https://github.com/litten/hexo-theme-yilia).
这是个github上的项目,用法下面有写,很简单的.







