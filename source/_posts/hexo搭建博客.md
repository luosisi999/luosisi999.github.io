---
title: hexo搭建博客
date: 2019-08-01 17:23:22
categories: 有关博客搭建
tags: 
- hexo
- 博客
---
### 搭建博客的步骤
[查看hexo官网: 帮助文档](https://hexo.io/zh-cn/docs/index.html)

### 一、建站
###### 1.安装node.js环境。
[点击安装](https://nodejs.org/en/)
###### 2.安装git环境
[点击安装](https://git-scm.com/)
###### 3.安装hexo
$ npm install -g hexo-cli
###### 4.基本命令操作
	- 创建博客系统
	hexo init “博客系统名”
	- 切换到博客目录
	cd 创建的博客名
	- 本地服务器启动
	hexo server 
	(若默认的4000 端口有问题执行下面)
	hexo server -p 5000 指定端口号为5000
<!--more-->
### 二、部署到github
###### 1.新建一个空的github仓库
命名：”github id”.github.io
###### 2.修改主站的配置文件(绑定github)
``` 
deploy:
type: git
repo: git@github.com:chibaobao/chibaobao.github.io.git

```
###### 3.安装一个自动提交插件
$ npm install hexo-deployer-git --save

### 三、创建一篇新博客，并部署
1. hexo new “博客名”
2. 执行命令提交
+  hexo generate 生成静态文件
+ hexo deploy –generate 将之前生成的静态文件部署到github

### 四、怎么给文档添加标签？
###### 1.博客主目录，执行命令hexo new page tags
###### 2.上述命名成功，找到 tags/index.md,修改如下。
```
title: 文章分类
date: 2017-05-27 13:47:40
type: "tags"
```
###### 3. 给文章添加“tags”属性,找到需要添加tag的文章。
```
---
title: jQuery对表单的操作及更多应用
date: 2017-05-26 12:12:57
categories: //分类
- web前端
tags://标签
- jQuery
- 表格
- 表单验证
---
```
同理添加分类是一样的，但是yilia没有分类这个功能