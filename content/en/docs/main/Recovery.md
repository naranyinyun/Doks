---
title: "Recovery"
description: "Recovery 模式是 Android 的一种模式, 可以修改手机的内部数据, 进行刷写等操作"
lead: "Recovery 模式是 Android 的一种模式, 可以修改手机的内部数据, 进行刷写等操作"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "main"
weight: 100
toc: true
---
## 通过 ADB 刷入 Recovery
首先, 在您的电脑上配置好 ADB 环境
将手机重启至 Fastboot 模式并连接电脑
在您的终端中输入 (PowerShell)
```
adb flash recovery [path];adb reboot recovery
```
这样, 您的手机就会重启至 Recovery 了
## 通过其他工具刷入 Recovery
使用诸如搞机助手, 秋之盒等带有 GUI 的工具箱刷入, 他们的使用方法非常简单, 相信您一看就会
我们不做过多介绍了
## 一些提示
1. 一旦刷入第三方 Recovery, 您就要考虑 AVB 的问题
2. 部分 ROM(MIUI, 自带 Recovery 的 ROM) 可能会覆盖您刷入的 Recovery, 使用 Magisk 实现防覆盖
