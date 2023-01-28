---
layout: post
title:  AndroidIDE-让手机写地牢Mod成为可能
tags: [2023,Java,IDEA,Termux,Github,Gradle,SetUp]
author: JDSALing
stickie: true
---

---
撰写于2023年1月28日--建议阅读时间：40分钟

---

## 阅前说明：
本教程主要针对于没有电脑想写地牢的朋友，虽然大家可以直接通过MT文件管理器什么的来逆向写牢。但这样门槛太高，且根本不利于大家学习。而且Smali本身也是Java的Davilk语言，因此各位应该在手机上写正向代码(Java),来自于印度的开发者开发了AndroidIDE,他可以让大家在手机上写地牢成为可能！

## 关于：Android Studio
我们一般简称它为AS，这个是电脑开发必备的软件。  
ADE和它类似。不过仍然有一些功能不齐全……
下面的表格应该会详细告诉你两个软件的比对情况(仅供参考)

|功能对比|AndroidStuido|AndroidIDE
|-|-|-
|代码补全|[√]|[√]
|代码查错|[√]|[√]
|断点调试|[√]|[x]
|版本控制|[√]|[x]
|Gradle|[√]|[√]
|高性能编辑|[√]|[√]
|Kotlin编码|[√]|[x]
|编译部署|[√]|[√]
|JDK-11|[√]|[√]
|JDK-17|[√]|[√]
|SDK|[√]|[√]

---

 从上表我们可以看出,ADE远远还没有AS强大。不过，这并不影响各位使用ADE!现在了解了他们究竟是什么后，准备部署吧！

## 1.开始部署：AndroidIDE
No.1-下载安装完AndroidIDE后，将会提醒你JDK和SDK尚未安装  
No.2-可以通过idesetup -c一键安装，但镜像默认外国的，需要科学上网




