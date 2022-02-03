---
cover: https://raw.githubusercontent.com/mengxiaozhi/dowload/gh-pages/image/worrld-edit-minecraft.png
title: 'WorldEdit: Bedrock Edition 基岩版小木斧使用教程'
date: 2022-02-03 15:03:25
categories:
- 游戏
tags:
- Minecraft
---
此版本仅限基岩版（包括手机，Windows 10以上PC）（疑似可使用Xbox，添加Realms后可在Switch和Playstaion）
下载地址：https://mcpedl.com/worldedit-be-addon/
官方文档（英文）：https://worldedit-be-docs.readthedocs.io/en/latest/
开源项目：https://github.com/SIsilicon/WorldEdit-BE
## 开始使用
在导入行为包并打算开始使用前请先把存档中的实验功能全部打开，以防止Add on之间的冲突或运行失败

官方在游戏中已经内置了使用手册，在游戏中的 设定>游戏指南>Quick Start
或者也可以到作者的网站上查看官方的使用手册
官方文档（英文）：https://worldedit-be-docs.readthedocs.io/en/latest/
但是目前官方尚未推出中文版，需具备一定英文基础

需要先通过添加builder标签的方式给玩家添加使用权限
```
/tag "玩家ID" add builder
```
添加完成后，拥有此builder标签的人就拥有小木斧的权限了。

在此版本的WorldEdit中，指令几乎全部继承了原版的指令，只是把开头的//改为了;
所以如果你用过原版WorldEdit，你将会很快上手
## 基础指令
取得小木斧
```
;wand #取得小木斧
```
取得其他工具（这些工具使用来代替指令的）
```
;kit #取得其他工具
```
设定第一个点
在潜行状态下使用小木斧右键点击方块（手机端轻点方块）
或者使用指令设定
```
;pos1 #设定第一个点
```
设定第二个点
在正常站立状态下使用小木斧右键点击方块（手机端轻点方块）
或者使用指令设定
```
;pos2 #设定第二个点
```
## 开始填充你的第一个方块
设定完两个点后使用以下格式添加方块

```
;set air #空气方块
```

与原版不同的是，此版本直接输入方块即可
假设方块的名字中有空格，即使用_下划线代替，例如

```
;set smooth_stone #平滑石头
```

架设你对你命令和方块名字不熟悉，那么可以使用此版本提供的kit工具进行使用
取得其他工具（这些工具使用来代替指令的）
```
;kit #取得其他工具
```