---
title: "发帖论坛"
summary: 一个基于OpenResty + lua + mysql + ngx-shared lor middleware jwt makedown文档格式 bootstrap 等技术。
description : 一个基于OpenResty + lua + mysql + ngx-shared lor middleware jwt makedown文档格式 bootstrap 等技术。
keywords : ["lua", "openresty", "发帖论坛", "评论",  "论坛", "帖子"] 
date: 2024-11-18
categories: ["lua"]
weight: 3
tags: ["案例","论坛", "lua"]
author: ["admin"]
series: ["系统"]
cover:
  image: posts/lua/openresty-china/images/2.webp
  caption: "lua [发帖论坛](#)"
  hidden: false ## 封面图是否隐藏
  hiddenInList: false ## 封面图是否 在列表隐藏
  hiddenInSingle: true ## 封面图是否 在单页隐藏
  alt: 发帖论坛
  # caption: 图片标题
  # width: 图片宽度
  # height: 图片高度
  # alignment: 图片对齐方式
ShowToc: true # 是否显示目录
TocOpen: false # 目录是否打开
---

## 项目介绍  
  - 一个运行在[OpenResty](http://openresty.org)上的发帖论坛。
  - 本项目前端部分基于 bootstrap

---

## 特点
- 简洁  
- 高性能
- 代码完全采用ngx-lua + mysql实现
- 来自饭总的[openresty-china](https://github.com/sumory/openresty-china)项目
---

## 描述
- 适用于公司内部论坛,随拿随用

---

## 案例项目图片展示
  #### 后台 
   ![1](./images/1.webp) 
   ![3](./images/2.webp)
   ![2](./images/0.webp)  
  
---


## 项目目录简介
```
app:          http api服务代码
lor:          http服务框架代码
resty:        第三方基础库代码
conf:         配置
``` 

---


## 安装
``` 
安装mysql 省略 导入数据库 conf/openresty_china_2022-04-24.sql 
[root@iZ~]#wget https://openresty.org/download/openresty-1.11.2.3.tar.gz
[root@iZ~]#tar xvf openresty-1.11.2.3.tar.gz
[root@iZ~]#cd openresty-1.11.2.3
./configure --with-luajit && make && make install
[root@iZ~]#cd /data/web
[root@iZ~]#git clone git@github.com:poembro/openresty-im.git 
[root@iZ~]#/usr/local/openresty/sbin/nginx -c /data/web/openresty-china/conf/nginx.conf
```
 

 