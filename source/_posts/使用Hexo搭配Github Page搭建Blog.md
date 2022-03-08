---
cover: >-
  https://raw.githubusercontent.com/mengxiaozhi/dowload/gh-pages/image/1*zGn8GFhpCNdbO3wSvJO2JQ.jpeg
title: 使用Hexo搭配Github Page搭建Blog
categories: 开发
tags:
  - 前端
  - Hexo
abbrlink: 46103
date: 2022-01-31 00:00:00
---
## 准备工具
1.安装node.js
2.安装hexo
3.安装git（选择性安装，因为hexo有插件可以直接上传Github）
4.一个Github账号用于创建库

## 需具备基础
1.html
2.css
3.markdown（主要写文章的标记语言，编写方便）

## 创建一个Github库
在Github中创建一个库，其中Repository name将会影响到后续网页的上传，请慎重填写。
![](https://raw.githubusercontent.com/mengxiaozhi/dowload/gh-pages/image/Screen%20Shot%202022-01-31%20at%206.37.25%20PM.png)

创建完库后的https链接记下来，后续上传网页将会用到
![](https://raw.githubusercontent.com/mengxiaozhi/dowload/gh-pages/image/Screen%20Shot%202022-01-31%20at%206.37.36%20PM.png)


## 安装node.js
进入https://nodejs.org/
![](https://raw.githubusercontent.com/mengxiaozhi/dowload/gh-pages/image/Screen%20Shot%202022-01-31%20at%203.02.20%20PM.png)
LTS:长期服务，较为稳定
Current:最新版本
建议下载LTS版本，搭建网站以稳为主。

可以选择直接下载安装包下载，也可以用指令搭配其他环境下载
https://nodejs.org/zh-tw/download/package-manager/

安装完后，检查node.js版本验证是否成功安装
```
npm -v  #检查npm版本号
node -v  #检查node.js版本号
```

## 安装Hexo
Hexo必须在具备node.js的环境中运行，所以必须执行上一步
在命令行中执行
```
npm install hexo-cli -g  #安装Hexo本体
```

## 创建第一个网页
初始化Hexo用于创建第一个页面
```
hexo init  #初始化Hexo
```
hexo init的后面也可以加一个文件夹名字用于创建一个新的空文件夹，比如在后面加一个blog，如果文件夹不是空的，hexo将初始化失败。
```
hexo init blog  #在blog文件夹初始化Hexo
```
## 写第一篇文章
```
hexo new <tittle> #创建一个新页面，<   >内为文章标题
```
如果你的主题有默认布局，则可以加上layout生成默认布局的页面
```
hexo new [layout] <title>
```
## 测试和编译
```
hexo s  #启用服务，http://localhost:4000/ 为默认地址
```
## 上传网页
在不使用git的情况下，单纯靠Hexo上传网页，需要先安装Hexo内的一个插件
```
npm install hexo-deployer-git --save  #安装hexo-deployer-git
```
安装完成后需到hexo的_config.yml配置文件进行GitHub库的设定
```yml
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: 'git'  #如果是上传到git，type类型填git
  repo: 'https://github.com/username/blog.git'  #这边填写的就是你创建完库后的http链接，直接复制粘贴即可。username填你的名字，blog是你的库，如果你的库就是你的名字则不需要username后面的内容，但最后都加.git
  brach: 'gh-pages'  #这边是你库的分支，选择你想上传的就好，一般填gh-pages
```
清除本地文件
```
hexo cl  #清除本地文件
```
编译生成静态网页文件
```
hexo g  #编译生成静态网页文件
```
将编译完成的静态文件上传至Github
```
hexo d  #上传至Github,第一次上传会要求登入账号
```
之后就完成啦～你的网站已经可以在Github上正常使用了～
## 推荐使用软件
1.Typora
Markdown语言的编辑器，可以很轻易的编写内容

2.Visual Studio Code
微软出品的编辑器，前端必备

