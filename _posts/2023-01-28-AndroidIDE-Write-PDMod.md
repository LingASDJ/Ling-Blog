---
layout: post
title:  AndroidIDE-让手机写地牢Mod成为可能-Demo(尚未完成)
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
|NDK|[√]|[x]

---

 从上表我们可以看出,ADE远远还没有AS强大。不过，这并不影响各位使用ADE!现在了解了他们究竟是什么后，准备部署吧！

# 1.开始部署：AndroidIDE-SDK
1.下载安装完AndroidIDE后，将会提醒你JDK和SDK尚未安装  

### 部署方法A:
使用反代Json+JDK11轻松配置：

#### 安卓11以上的策略：
其实和安卓10配置差不多，但如果是本地，Android/Data区默认无法访问，请根据自身机型访问。(但内存框架必定可以访问！)

## β：快速NET部署:

A.首次进入你将会看见这个界面：
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set1.jpg">
B.当你点击确定后应该会看见这个界面：
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set1.5.jpg">
C.快速配置你的SDK：  
```bash
idesetup -m url http://39.105.229.249/ftp/ling/json/manifest.json
```
D.如下图所示：
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set2.jpg">

E.当你回车后所有的提醒都输入Y
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set3.jpg">

F.当出现<b><font color="#00cc00">You are ready to go</font></b>说明你的SDK环境已经配置完成
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set4.jpg">

## γ：本地手动部署:

1.首先清楚QQ的下载路径：
### A.常规QQ:
/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/
### B.TIM-QQ
/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/

2.这里我们以常规QQ为例子：
```bash
### 如果显示Permission Denied则说明是安卓11（请复制需要的文件到可以访问的文件夹中）

### Android/data/ 在安卓11以上无法随便访问

idesetup -m file:///storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/manifest.json

```

3.当出现<b><font color="#00cc00">You are ready to go</font></b>说明你的SDK环境已经配置完成
<img src="http://39.105.229.249/ftp/ling/cdnpng/adepng/Set4.jpg">

# 2.开始部署：AndroidIDE-JDK
在群文件中下载了JDK11包或者是在下方链接获取到包后如何使用？

### A.QQ群文件下载部署流程

这里我们以常规QQ为例子：

```bash
### 如果显示Permission Denied则说明是安卓11（请复制需要的文件到可以访问的文件夹中）

### Android/data/ 在安卓11以上无法随便访问

cd /storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/

### 复制JDK11到Home目录

cp jdk11-aarch64.tar.xz ~

### 跳转到Home目录
cd ~

### 解压这个包
tar xvf jdk11-aarch64.tar.xz

### 安装VIM编辑器
pkg install vim -y

### 创建环境变量配置文件
vim ~/.bash_profile

### 写进去
export JAVA_HOME=~/jdk/openjdk-11.0.1
export PATH=$PATH:$JAVA_HOME/bin

### 按下面的ESC，并输入:wq
:wq

```

# 3.开始部署：AndroidIDE-SHPD

在群文件下载ADE优化版，并打开项目，
然后再等待自行SYNC完成……

### 教程尚未完成-Demo















