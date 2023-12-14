---
layout: post
title:  Pixel Dungeon-多语言逆向指南
tags: [Java,Gradle,IDEA,经验交流,Smali,MT文件管理器]
author: jdsaling
stickie: true
---

---
撰写于2022年10月18日--建议阅读时间：40分钟

# 目录-索引：
<font id="top"></font>
<h2><a href="#note">1.多语言逆向指南</a></h2>
<h2><a href="#kite">2.PD10Tools使用指南</a></h2>

---
## 情景引入：
<font id="note"></font>
有一个比较好玩的PD是基于破碎的版本，然而作者将语言按钮和语言自适应的环境都给去掉了，而源代码需要一台电脑才能编译。但我现在<font color="#ff00000"><b>只有手机</b></font>，我是不是无法进行我的汉化工作了？答案是否定的，基于破碎的地牢99%都不会再去移除多语言框架，因此，只需要通过<font color="#99d921f"><b>MT文件管理器</b></font>进行一些代码的优化与调整，方可获得一个汉化版。

----

## 准备工作:
> 诚然，<font color="#ff00ff"><b>良好的学习态度是进步的根本因素。</b></font>  
虽然Smali是Java的逆向语言，它偏向于汇编，它也被称为<font color="#ff00000"><b>Davlik的寄存器语言</b></font>  
因此，各位需要准备的软件为以下:
* MT文件管理器  
---
嗯，没错，只需要它。就可以完成我们的汉化工作。

## 方案步骤:

---
### 1.定位APK，了解Class.dex文件:
#### No.1-打开你的MT文件管理器，找到对应需要修改的安装包：
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-1.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-2.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-3.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-4.jpg">

---
### 2.寻找指定类名，修改Smali代码:
#### No.2-语言文件的位置说明：
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-5.jpg">

#### No.3-举个例子（RKPD2)：
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-6.jpg">

#### No.4-添加语言文件（RKPD2)：
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-7.jpg">
温馨提示：RKPD2作者默认只是去除了语言的自适应环境和语言按钮，并没有直接删除除英文的其他语言文件。
因此这里才可以投机取巧的不修改这里，如果只有英文文件则请自行添加zh文件（zh文件最好和此MOD版本的底层破碎对应)<font color="afbfcf"><b>可以到Github去看此版本的底层破碎版本，或者查看游戏内部的更新记录</b></font>

#### No.5-DEX实战修改（RKPD2)：
### 1.点击搜索功能，发起新搜索，搜索类型选择类名，搜索类名为"<font color="cf5f72"><b>Languages</b></font>"的类。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-8.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-9.jpg">

### 2.点击此名叫"<font color="cf5f72"><b>Languages</b></font>"的类。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-10.jpg">

### 3.在"<font color="cf5f72"><b>Languages</b></font>"内寻找这个结构的代码，找不到的话可以看看下一步的搜索功能。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-11.jpg">

### 3.5.地牢语言系统工作流程:(流程图制作于BoardMixed平台)：
<img src="https://jdsalingzx.top/assets/img/mtsmali/langues.png">

### 4.本步骤仅针对于查找<font color="cf5f72"><b>“中文”</b></font>后能找到后实现的一个小步骤，否则，本步可以被忽略。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-12.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-13.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-14.jpg">

### 5.上述操作全部完成后，<font color="cf5f72"><b>保存并退出</b></font>，千万不要手残点击<font color="725fbf"><b>直接退出</b></font>！！！，后面也是按照图片来，点击<font color="cf5f72"><b>确定</b></font>，千万别点击取消！！！<font color="cf5f72"><b>（如果点错一个，前面的操作全部成为无用功！！！）</b></font>
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-15.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-16.jpg">

### 6.APK共存，主要是将原版和汉化版区分开（此操作可以忽略）但是忽略的话，因为<font color="cf5f72"><b>签名不一致</b></font>将会导致卸载原版才能安装汉化版，所以仍然建议共存APK。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-17.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-18.jpg">

### 7.安装共存好的APK，并进入游戏查看最终效果
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-19.jpg">
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-20.jpg">

### 8.小结 看似复杂，实际上只需要几分钟就能完成的操作。这篇教程主要是想帮助各位想汉化的志同道合的朋友。下图为本章小结，可以看看，并消化一下上面谈到的东西和知识点。
<img src="https://jdsalingzx.top/assets/img/mtsmali/smali-end.jpg">

---
<font id="kite"></font>
---
<h2><a href="#top">返回目录索引区域</a></h2>

---

### <b><font color="00ffad">追加内容：PD10Tools使用指南:</font></b>
---
## <font color="00ffad">情景引入：</font>
某汉化者成功的汉化了一款地牢，然而却漏翻了一些东西。若手动查找起来势必是事倍功半，于是，在万般困难的境地，<font color="00ffad">PD10Tools</font>在Const的手中诞生，并造福广大地牢汉化者(编不下去了)。

软件布局说明:
<img src="https://jdsalingzx.top/assets/img/mtsmali/pd-tool1.jpg">

当选择了两个文件后的功能为：
<img src="https://jdsalingzx.top/assets/img/mtsmali/pd-tool2.jpg">

这三个按钮都会额外生成一个文件出来:
<img src="https://jdsalingzx.top/assets/img/mtsmali/pd-tool5.jpg">

常见问题：
### Source language file path is empty. 
* 源语言的目录为空（通过SEL选择上）
<img src="https://jdsalingzx.top/assets/img/mtsmali/pd-tool3.jpg">

### Target language file path is empty. 
* 目标语言的目录为空（通过SEL选择上）
<img src="https://jdsalingzx.top/assets/img/mtsmali/pd-tool4.jpg">

### 参考资料
本文章完全原创！！！

#### By JDSA Ling-Ling Book Blog

---
### 声明：若要转载此文章，请注明出处，非常感谢
---