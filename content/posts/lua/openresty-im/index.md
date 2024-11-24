---
title: "web聊天软件"
summary: 一个运行在OpenResty上的web聊天软件。
description : 一个运行在OpenResty上的web聊天软件。
keywords : ["lua", "OpenResty", "web聊天软件"] 
date: 2024-10-18
categories: ["lua"]
weight: 3
tags: ["案例","OpenResty", "lua"]
author: ["admin"]
series: ["lua"]
cover:
  image: posts/lua/openresty-im/images/0.png
  caption: "OpenResty  [web聊天软件](#)"
  hidden: false ## 封面图是否隐藏
  hiddenInList: false ## 封面图是否 在列表隐藏
  hiddenInSingle: true ## 封面图是否 在单页隐藏
  alt: web聊天软件
  # caption: 图片标题
  # width: 图片宽度
  # height: 图片高度
  # alignment: 图片对齐方式
ShowToc: true # 是否显示目录
TocOpen: false # 目录是否打开
---


# OpenResty IM 

一个运行在[OpenResty](http://openresty.org)上的基于[lor](https://github.com/sumory/lor)编写的web聊天软件。

- 完全基于OpenResty
- 存储采用MySQL，ngx.shared.DICT(共享内存区块) 
- 方案: 服务端接收消息后 临时存储，客户端携带偏移位置一直读取最新。


###
![im](./images/0.png)
### 安装

- 首先安装OpenResty(可以按自己的需要安装)

```
    [root@iZ~]#yum install libtermcap-devel ncurses-devel libevent-devel \
    readline-devel pcre-devel openssl openssl-devel 
     
    [root@iZ~]#wget https://openresty.org/download/openresty-1.11.2.3.tar.gz
    [root@iZ~]#tar xvf openresty-1.11.2.3.tar.gz
    [root@iZ~]#cd openresty-1.11.2.3
    ./configure --with-luajit && make && make install


    注意:  有个 resty-uuid  需要引用 libuuid.so 动态库
    打印log提示信息是这样的:
    libuuid.so: cannot open shared object file: No such file or directory
    解决方法: 
    [root@iZ~]#yum install libuuid libuuid-devel 
    [root@iZ~]#ln -s /lib64/libuuid.so.1.3.0 /usr/lib64/libuuid.so
    [root@iZ~]#ln -s /usr/lib64/libuuid.so /usr/local/openresty/lualib/resty/libuuid.so
    [root@iZ~]# ldconfig
    
    
    [root@iZ~]#yum install ImageMagick ImageMagick-devel  # imagemagick c 库
    [root@iZ~]#yum install GraphicsMagick-devel           # GraphicsMagick c 库

```
 
- 目前只需要一张表用户表，将其导入到MySQL   (按需处理多余字段)

```
	CREATE TABLE `mg_user_member` (
	  `uid` int(10) unsigned NOT NULL AUTO_INCREMENT COMMENT '用户UID',
	  `admin_id` int(10) NOT NULL DEFAULT '0' COMMENT '0为非管理员，1为管理员',
	  `group_id` tinyint(1) NOT NULL DEFAULT '1' COMMENT '类型 1-普通 2-客服 3-管理',
	  `nickname` varchar(30) NOT NULL DEFAULT '' COMMENT '昵称',
	  `mobile` varchar(15) NOT NULL DEFAULT '' COMMENT '手机号码',
	  `email` varchar(75) NOT NULL DEFAULT '' COMMENT '邮箱',
	  `password` varchar(256) NOT NULL COMMENT '密码',
	  `passkey` varchar(16) NOT NULL DEFAULT '' COMMENT '密码key',
	  `regtime` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '注册时间',
	  `regip` varchar(20) DEFAULT '0' COMMENT '注册IP',
	  `logintime` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '注册时间',
	  `loginip` bigint(20) DEFAULT '0' COMMENT '注册IP',
	  `face` varchar(200) NOT NULL DEFAULT '' COMMENT '头像', 
	  `hide` tinyint(1) NOT NULL DEFAULT '0' COMMENT '是否隐藏信息 1-是　0-否', 
	  `sex` tinyint(1) NOT NULL DEFAULT '1' COMMENT '性别 1-男 0-女',
	  `province` varchar(30) NOT NULL DEFAULT '' COMMENT '省份',
	  `city` varchar(30) NOT NULL DEFAULT '' COMMENT '城市',
	  `signature` varchar(255) NOT NULL DEFAULT '' COMMENT '签名',
	  `lasttime` int(10) NOT NULL DEFAULT '0' COMMENT '最后发言时间',   
	  `qq` varchar(20) NOT NULL DEFAULT '' COMMENT 'QQ号码', 
	  `iskick` tinyint(1) NOT NULL DEFAULT '0' COMMENT '是否已被踢 1-是 0-否',
	  `visible` tinyint(1) NOT NULL DEFAULT '1' COMMENT '状态 1-显示 0-删除',
	  `remark` varchar(255) DEFAULT NULL,
	  `realname` varchar(30) DEFAULT '' COMMENT '真实姓名',
	  PRIMARY KEY (`uid`),
	  KEY `regtime` (`regtime`),
	  KEY `g` (`state`,`hide`,`lv`),
	  KEY `mobile` (`mobile`) USING BTREE
	) ENGINE=MyISAM AUTO_INCREMENT=1225 DEFAULT CHARSET=utf8 ROW_FORMAT=DYNAMIC COMMENT='用户表';

```


- 修改配置文件`app/config/config.lua`为本地对应配置，强烈建议将以下值修改为不同配置
	- session_secret 用于session加密 (暂时不用) 
	- pwd_secret 用户数据库密码存储时加密   
	- mysql 配置
	
- 配置静态文件目录，这个目录用于存放用户上传的头像、聊天图片等
	- 默认的目录为 /data/cluster/web/src/html/openresty/im/app/static/，如非必要建议目录和我一致，并保证有写权限
	- 若要修改上述默认目录，请修改app/config/config.lua中的upload_config.dir和nginx配置文件中的$static_files_path的值，保证两个值一致
 
 
- 为了省事,建议项目直接解压在 /data/cluster/web/src/html/openresty/ 目录下



cd /data/web/openresty-im/proto
protoc -o logic-goim.pb logic-goim.proto






CREATE TABLE `mg_user` (
  `id` int(10) unsigned NOT NULL AUTO_INCREMENT COMMENT '用户UID',
  `nickname` varchar(30) NOT NULL DEFAULT '' COMMENT '昵称',
  `mobile` varchar(15) NOT NULL DEFAULT '' COMMENT '手机号码',
  `password` varchar(256) NOT NULL COMMENT '密码',
  `user_id` bigint(11) NOT NULL COMMENT 'user_id',
  `regtime` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '注册时间',
  `regip` varchar(20) NOT NULL DEFAULT '0' COMMENT '注册IP',
  `logintime` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '注册时间',
  `loginip` bigint(20) NOT NULL DEFAULT '0' COMMENT '注册IP',
  `face` varchar(200) NOT NULL DEFAULT '/static/wap/img/portrait.jpg' COMMENT '头像',
  `sex` tinyint(1) NOT NULL DEFAULT '1' COMMENT '性别 1-男 0-女',
  `visible` tinyint(1) NOT NULL DEFAULT '1' COMMENT '状态 1-显示 0-删除',
  `remark` varchar(255) NOT NULL DEFAULT '',
  `realname` varchar(30) NOT NULL DEFAULT '' COMMENT '真实姓名',
  PRIMARY KEY (`id`),
  UNIQUE KEY `user_id` (`user_id`),
  KEY `mobile` (`mobile`)
) ENGINE=MyISAM AUTO_INCREMENT=4 DEFAULT CHARSET=utf8 ROW_FORMAT=DYNAMIC COMMENT='用户表';


CREATE TABLE `mg_group` (
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT COMMENT '群组id',
  `group_id` bigint(20) unsigned NOT NULL DEFAULT '0' COMMENT '群组id',
  `name` varchar(20) COLLATE utf8mb4_bin NOT NULL COMMENT '组名',
  `dateline` int(11) unsigned NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin COMMENT='群组';

CREATE TABLE `mg_group_user` (
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT COMMENT '自增主键',
  `group_id` bigint(20) unsigned NOT NULL COMMENT '组id',
  `user_id` bigint(20) unsigned NOT NULL COMMENT '用户id',
  `label` varchar(20) COLLATE utf8mb4_bin NOT NULL COMMENT '用户在群组的昵称',
  `dateline` int(11) unsigned NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`),
  UNIQUE KEY `uk_group_user` (`group_id`,`user_id`) USING BTREE,
  KEY `idx_user_id` (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin COMMENT='群组成员关系';

