---
title: "合成大西瓜"
summary: 一个基于phaser3 + javascript +  matter 物理引擎 等技术，实现的休闲小游戏合成大西瓜。
description : 一个基于phaser3 + javascript +  matter物理引擎 等技术，实现的休闲小游戏合成大西瓜。
keywords : ["phaser3", "javascript", "matter"] 
date: 2024-10-18
categories: ["phaser"]
weight: 3
tags: ["案例","小游戏", "phaser"]
author: ["admin"]
series: ["game"]
cover:
  image: posts/phaser/hexigua/images/0.png
  caption: "phaser [合成大西瓜](#)"
  hidden: false ## 封面图是否隐藏
  hiddenInList: false ## 封面图是否 在列表隐藏
  hiddenInSingle: true ## 封面图是否 在单页隐藏
  alt: 合成大西瓜
  # caption: 图片标题
  # width: 图片宽度
  # height: 图片高度
  # alignment: 图片对齐方式
ShowToc: true # 是否显示目录
TocOpen: false # 目录是否打开
---



## 项目介绍
- 一个 Phaser 3 开发的h5休闲小游戏合成大西瓜， 一共有11个类型的水果，随机掉落后组合， 最后合成最大的11号西瓜。
- 目前是 matter物理引擎  项目作者是 [eijil](https://github.com/eijil/hexigua) 非常好的参考学习案例


## 实现方案
- 采用 phaser3 + ts语言编写
- 采用 matter物理引擎，放射粒子效果动画 
- 采用 rollup  打包

## 案例项目图片展示
  #### 游戏 
   ![1](./images/1.png) 
   ![3](./images/2.png)
   ![2](./images/0.png)  
   ![2](./images/3.png)  


# Phaser 3 TypeScript Project Template

## demo

[http://hexigua.surge.sh/](http://hexigua.surge.sh/)

## Available Commands

| Command | Description |
|---------|-------------|
| `npm install` | Install project dependencies |
| `npm run watch` | Build project and open web server running project, watching for changes |
| `npm run dev` | Builds project and open web server, but do not watch for changes |
| `npm run build` | Builds code bundle with production settings (minification, no source maps, etc..) |

## Writing Code

After cloning the repo, run `npm install` from your project directory. Then, you can start the local development
server by running `npm run watch`. The first time you run this you should see the following demo run:


