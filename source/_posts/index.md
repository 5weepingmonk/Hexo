
---
title: 关于本博客   
date: 2200-11-7 08:55:29   
categories: 介绍
tags : 介绍   
toc: true 
---

这篇博客是为了自己之前的主站而创建的，因为我保存住原本Hexo博客中的主要东西比如:

    _config.yml，theme/，source/，scaffolds/，package.json，.gitignore，
    
所以创建本博客来继续作为本作者的笔记

原博客地址:[传送门](https://tugohost.github.io)

来说下如何在换电脑或者换硬盘的情况下更新博客吧
摘自[知乎](https://www.zhihu.com/question/21193762)

### 总结：
    _config.yml，theme/，source/，scaffolds/，package.json，.gitignore，是需要拷贝的。

再讨论下哪些文件是不必拷贝的，或者说可以删除的：首先是.git文件，无论是在站点根目录下，还是主题目录下的.git文件，都可以删掉。然后是文件夹node_modules（在用npm install会重新生成），public（这个在用hexo g时会重新生成），.deploy_git文件夹（在使用hexo d时也会重新生成），db.json文件。其实上面这些文件也就是.gitignore文件里面记载的可以忽略的内容。

### 总结：
    .git/，node_modules/，public/，.deploy_git/，db.json文件需要删除。

1. 在git bash中切换目录到新拷贝的文件夹里，使用 npm install 命令，进行模块安装。很明显我们这里没用hexo init初始化，因为有的文件我们已经拷贝生成过来了，所以不必用hexo init去整体初始化，如果不慎在此时用了hexo init，则站点的配置文件_config.yml里面内容会被清空使用默认值，所以这一步一定要慎重，不要用hexo init。

2. 安装其他的一些必要组件，如果在node_modules里面有的，就不要重复安装了：
    
    （1）为了使用hexo d来部署到git上，需要安装
    npm install hexo-deployer-git --save
    （2）为了建立RSS订阅，需要安装
    npm install hexo-generator-feed --save
    （3）为了建立站点地图，需要安装
    npm install hexo-generator-sitemap --save
    插件安装后，有的需要对配置文件_config.yml进行配置，具体怎么配置，可以参考上面插件在github主页上的具体说明
    7、使用hexo g，然后使用hexo d进行部署，如果都没有出错，就转移成功了！

