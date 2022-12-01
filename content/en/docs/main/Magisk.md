---
title: "Magisk"
description: "One page summary of how to start a new Doks project."
lead: "Magsik 是适用于 Android 的一种框架, 通过挂载自定义的分区实现的 Systemless 特性, Magisk 可以更安全, 更强大实现一系列功能, 当然, 不止 Root"
date: 2020-11-16T13:59:39+01:00
lastmod: 2020-11-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 110
toc: true
---
## 通过第三方 Recovery 刷入
从 GitHub 获取 [Magisk](https://github.com/topjohnwu/Magisk) 并将其重命名为 Install.zip
重启设备至 Recovery 并将 `Install.zip` 传入手机

TWRP:
1. 选择 ` 刷入 `
2. 选择 `Install.zip`
3. 滑动确认

## 通过 Fastboot 刷入
提取 boot(可以使用我们提供的方式提取, 也可以从刷机包中获取)
打开 Magisk Manager，选择安装, 选择 ` 选择并修补一个文件 `，选择你的 Boot 并等待修补完成
重启至 Fastboot 并刷入 Boot

ADB:
```
fastboot flash boot [path]
```

## 一些提示
1. 在部分 ROM 上, 刷入 Magsik 后 Magisk Manager 可能无法识别, 刷入 Magsik 24.3 即可
2. 不要刷入他人提供的 Boot, 您无法确认他适用于您的设备
3. 同样的, 若刷入 Magsik 后无法启动设备, 您需要考虑 AVB 的问题