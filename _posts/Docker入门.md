---
layout: post
title: docker入门总结
date: 2020-06-08
---

# Docker入门
## 如何使用docker？
    docker在后台运行着一个docker daemon的进程，用户通过docker CLI与其交互。
    docker daemon运行时使用默认配置,当然也是可以进行用户配置。查询官方文档地址：https://docs.docker.com/config/daemon/
    可以获取如何进行配置的方法：
    1，当然可以通过CLI传递配置参数；2，创建一个JSON配置文件daemon.json添加配置信息,在linux系统中默认文件路径为/etc/docker/daemon.json，
    windows的默认文件路径为C:\Users\Administrator\.docker\daemon.json。
    至于有哪些配置选项，可以通过查询官方文档或者dockerd --help CLI命令获取。
    在国内由于网络原因，一般都要进行镜像仓库mirrors的配置，不然docker拉取镜像的速度没法忍受。在JSON配置文件中添加
    "registry-mirrors": ["镜像加速地址XXX"]字段。
    
## 镜像
    1,什么是镜像？
        简单来说，镜像就是一个打包的文件系统，一个应用运行时所需要的所有文件都包含其中。
    2，构建mysql数据库镜像。
        
