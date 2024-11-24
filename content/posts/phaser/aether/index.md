---
title: "RPG闯关游戏"
summary: 一个基于phaser3 + javascript + Tiled场景地图 等技术，实现的RPG 闯关卡类型的小游戏。
description : 一个基于phaser3 + javascript + Tiled场景地图 等技术，实现的RPG 闯关卡类型的小游戏。
keywords : ["phaser3", "javascript", "Tiled", "闯关","RPG"] 
date: 2024-10-18
categories: ["phaser"]
weight: 3
tags: ["案例","小游戏","RPG", "phaser"]
author: ["admin"]
series: ["game"]
cover:
  image: posts/phaser/aether/images/0.png
  caption: "phaser [RPG闯关游戏](#)"
  hidden: false ## 封面图是否隐藏
  hiddenInList: false ## 封面图是否 在列表隐藏
  hiddenInSingle: true ## 封面图是否 在单页隐藏
  alt: RPG闯关游戏
  # caption: 图片标题
  # width: 图片宽度
  # height: 图片高度
  # alignment: 图片对齐方式
ShowToc: true # 是否显示目录
TocOpen: false # 目录是否打开
---


## 项目介绍
- 一个 Phaser 3 开发的 RPG闯关游戏，通用化场景地图，怪物坐标 掉落回血物品及坐标等，支持小白用户使用  Tiled 自定义 各个关卡。
- 目前是 aether 项目的改版，还处于开发阶段 


## 实现方案
- 采用 phaser3 + ts 混合 js 语言编写
- 采用 Tiled 编辑地图，以及行走区域 
- 采用 rollup  打包

## 案例项目图片展示
  #### 游戏 
   ![1](./images/1.png) 
   ![3](./images/2.png)
   ![2](./images/0.png)  
   ![2](./images/3.png)  

## Available Commands (可用命令)

| Command | Description |
|---------|-------------|
| `npm install` | Install project dependencies |
| `npm run watch` | Build project and open web server running project, watching for changes |
| `npm run dev` | Builds project and open web server, but do not watch for changes |
| `npm run build` | Builds code bundle with production settings (minification, no source maps, etc..) |

## Writing Code （编写代码）

After cloning the repo, run `npm install` from your project directory. Then, you can start the local development
server by running `npm run watch`. The first time you run this you should see the following demo run:


