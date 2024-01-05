---
layout: post
title:  AndroidIDE-让手机写地牢Mod不再是梦!(2024-重制版)
tags: [2024,Java,IDEA,Termux,Github,Gradle,SetUp]
author: JDSALing
stickie: true
---

---
撰写于2024年1月6日--建议阅读时间：10分钟

---

## 阅前说明：
本教程基于ADE2.6.1说明，从本版本开始，我们的宗旨是：自动化AUTO！

# 1.开始部署：AndroidIDE-SDK
1.下载安装完AndroidIDE后，将会提醒你JDK和SDK尚未安装

# 线上部署方法(推荐)：

## 1.ADE基础部署
进入终端后，输入以下指令：

```bash
wget https://www.pd.qinyueqwq.top/ftp/pd/ade/idesetupcn -O $SYSROOT/bin/idesetup && chmod +x $SYSROOT/bin/idesetup
```

下载完毕后：
输入 `idesetup` 回车 输入 Y 再次回车即可

注意：  
中途出现的第1个提示直接按回车，第2个提示输入Y再按回车。   
【其他询问请根据中文提示进行操作】


当出现以下图片，代表基础部署已经完成。

<img src="https://rust.coldmint.top/ftp/ling/cdnpng/ready.jpg">


## 2.下载优化版
目前提供两个优化版：   
分别是1.4.3和2.2.1
要想部署他们，  
请在终端中输入指令：   

```bash
### 2.2.1
git clone https://gitee.com/LingASDJ/SHPD-ADE-PACKAGE.git --branch 2.2.1-ADE /storage/emulated/0/AndroidIDEProjects/SHPD-ADE-2.2.1
```

```bash
### 1.4.3
git clone https://gitee.com/LingASDJ/SHPD-ADE-PACKAGE.git --branch 1.4.3-ADE /storage/emulated/0/AndroidIDEProjects/SHPD-ADE-1.4.3
```

1.下载完毕后，打开AndroidIDEProjects/SHPD-ADE-2.2.1(这里以221为例子)，    
等待初始化同步，并等待构建完毕。  

2.使用含有黑色边框的播放按钮输入android:assembleDebug--(其实默认就是这个)，    
并勾选， 然后点绿色播放按钮打包

3.如果在打包遇到错误，请再次点击绿色播放按钮，  
由于安卓近期安全性变化，  
首次构建成功后不会呼出安装管理器界面，    
可以再次点击绿色播放按钮强制呼出。也可以通过文件管理找到apk。  

例如上面：如果根路径是：   
/storage/emulated/0/AndroidIDEProjects/SHPD-ADE-2.2.1/

那么apk的位置在：   
/storage/emulated/0/AndroidIDEProjects/SHPD-ADE-2.2.1/android/build/outputs/apk/debug/

优化版已集成崩溃报告，更多地形，字段缺失检查器。祝各位开发愉快。

# 本地部署方法(不推荐)：

## 1.ADE基础部署
1.在群文件下载idesetupcn   
2.cd到对应目录，输入 `idesetupcn` 等待部署完成

## 2.部署优化版
1.在群文件下载ADE优化版   
2.解压到/storage/emulated/0/AndroidIDEProjects/中   
3.等待初始化同步，并等待构建成功

4.使用含有黑色边框的播放按钮输入android:assembleDebug--(其实默认就是这个)，   
并勾选， 然后点绿色播放按钮打包

5.如果在打包遇到错误，请再次点击绿色播放按钮，    
由于安卓近期安全性变化，    
首次构建成功后不会呼出安装管理器界面，    
可以再次点击绿色播放按钮强制呼出。也可以通过文件管理找到apk。  

例如上面：如果根路径是：  
/storage/emulated/0/AndroidIDEProjects/SHPD-ADE-2.2.1/

那么apk的位置在：  
/storage/emulated/0/AndroidIDEProjects/SHPD-ADE-2.2.1/android/build/outputs/apk/debug/

# 4.部署 Release 包

<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release1.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release2.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release3.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release4.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release5.jpg">
<img src="https://rust.coldmint.top/ftp/ling/cdnpng/adepng/release6.jpg">
