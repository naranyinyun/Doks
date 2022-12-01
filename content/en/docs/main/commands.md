---
title: "Third-Party ROM"
description: "Doks comes with commands for common tasks."
lead: "第三方 ROM 通常指类原生, 官改等非 OEM(原始设备制造商) 提供的操作系统"
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 130
toc: true
---
## 通用方法
在刷入第三方 ROM 之前, 有一些事项需要确认
- 设备 Bootloader 已解锁
- 有第三方 Recovery

刷入方法
1. 刷入适用的第三方 Recovey
2. 重启至 Recovery
3. 刷入 ROM
4. 双清并格式化 Data

跳过 Google 验证
在第三方 Recovery 的终端内输入
```
dd if=/dev/zero of=/dev/block/by-name/frp
```

## 基于 Android 11,MIUI 12.5(R-OSS) 的动态非 CFW ROM 的一些提示
1. Recovery 需要使用动态分区专用的 Recovery
2. 刷入后可以直接刷入其他动态 ROM, 无需再次刷入 MIUI
3. 切换到非动态 ROM 需要先卡刷 / 线刷回 MIUI
4. Recovery 在 Android 12L 上的 Data 解密可能不工作

## 基于 Android11,MIUI 12.5 的非动态非 CFW ROM 的一些提示
1. 切换至其他非动态 ROM 时直接刷入即可, 切换到动态 ROM 需要刷入 MIUI 再刷入 ROM
2. Recovery 在 Android 13 上可能无法格式化 Data


