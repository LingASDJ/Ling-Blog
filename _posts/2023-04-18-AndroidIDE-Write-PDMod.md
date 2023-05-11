---
layout: post
title:  AndroidIDE-让手机写地牢Mod成为可能！-初步配置
tags: [2023,Java,IDEA,Termux,Github,Gradle,SetUp]
author: JDSALing
stickie: true
---

---
撰写于2023年4月18日--建议阅读时间：40分钟

---

欢迎加入AndroidIDE-PD/Dev讨论群，我们的宗旨是：  
为想写地牢而无电脑的朋友创造更多可能。
<h2><a href="https://jq.qq.com/?_wv=1027&k=DOm63Y34">立即加入群聊：731514401</a></h2>

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

## α：官方部署策略--需要科学上网
推荐的梯子：
[Geph-迷雾通](https://jdsalinghub.top/geph-official/geph4-client/wiki/%E8%BF%B7%E9%9B%BE%E9%80%9A%EF%BC%88%E5%85%8D%E7%BF%BB%E5%A2%99%E9%95%9C%E5%83%8F%EF%BC%89)
```bash
### 速度慢,并不推荐此方法
idesetup -c -j 11
```

## β：本地手动部署:

1.首先清楚QQ的下载路径：
### A.常规QQ:
/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/
### B.TIM-QQ
/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/

2.这里我们以常规QQ为例子：
```bash
### 如果显示Permission Denied则说明是安卓11（请复制需要的文件到可以访问的文件夹中）

### Android/data/ 在安卓11以上无法随便访问

idesetup -m file:///storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/install-patch.json -j 11

```

3.当出现<b><font color="#00cc00">You are ready to go</font></b>说明你的SDK环境已经配置完成
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set4.jpg">

# 2.开始部署：AndroidIDE-SHPD

1.在群文件下载ADE优化版，并打开项目，然后再等待自行SYNC完成……
如下图所示：
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set8.jpg">

## 特别提醒：
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set9.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set10.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set11.jpg">

---

<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set12.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set13.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set14.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set15.jpg">

1.5.出现该界面后表示项目正在开始初始化：
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set5.jpg">

2.出现该界面后表示项目已经初始化完成：

<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set6.jpg">

3.可以尝试Run Build,理论上应该跑得起来。
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set7.jpg">

4.如果出现如下图所示，则说明APK包编译成功：
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set16.jpg">

5.DEBUG-APK的保存路径：  
/storage/emulated/0/AndroidIDEProjects/shattered-pixel-dungeon/android/build/outputs/apk/debug/

可以在这里找到你的DEBUG包，如下图所示：
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/Set17.jpg">


# 4.部署 Release 包

<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release1.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release2.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release3.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release4.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release5.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release6.jpg">













