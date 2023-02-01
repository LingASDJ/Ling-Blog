---
layout: post
title:  利用Exe4J & Inno Setup 将JAR编译为EXE (实现无JRE/JDK)
tags: [Java,Gradle,IDEA,Exe4J,Inno Setup]
author: jdsaling
---

---
撰写于2022年12月2日--建议阅读时间：30分钟
## 情景引入：
一款比较好玩的游戏是需要JRE的运行库支撑的，你的朋友Fang是个电脑小白~，不会安装JRE运行库。并且这人是个懒鬼……  (本故事纯属虚构，如有雷同，概不负责)
于是，为了能和朋友愉快游玩此游戏。你需要进行<font color="##00ff00">JRE转EXE并No JRE(即开即用，无需JRE安装)</font>.

## 准备工作：
* JRE运行库(32位或64位)
* EXE4J
* Inno SetUp

## 方案步骤：
* 1.确保你拥有一个JRE运行库（32位或64位均可)
* 2.打开EXE4J,确保能看见下面的界面：
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j1.png">
点击<font color="##689f0a">Change License</font>或者 <font color="##689f0a">Enter License</font>进行用户本地注册
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j2.png">

### 密钥大全，任选一个复制(均可使用)/适用于EXE4J-V8.0：

~~~log
A-XVK209982F-1y0i3h4ywx2h1
~~~
~~~log
A-XVK267351F-dpurrhnyarva
~~~
~~~log
A-XVK249554F-pllh351kcke50
~~~

* 3.注册成功后，点击下一步，开始进行EXE4J的转换：  
（若无特殊说明，均按照图示进行）
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j3.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j4.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j5.png">

#### 特别说明：这里如果是64位架构的软件请记得勾选此类：

<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j6.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j7.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j8.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j9.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j10.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j11.png">

接下来的全部下一步，等待EXE生成成功。
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j12.png">
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j13.png">

### 至此，JAR转EXE就全部完成，然后我们应该如何NoJRE/JDK呢？

# No JRE/JDK 的方法：
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j14.png">
1.请确保你的文件是新建的一个文件夹，然后将你选择的JDK/JRE放入进去。

<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j15.png">
2.并在第6区域的<font style="font-weight:700">Search Sequence</font>添加对应的JDK/JRE运行文件夹。<br>
<span>(<font color="##ff0000">警告：首次请先删除Search Windows registry外的所有东西，再添加JDK/JRE</font>.)</span>

3.进行编译打包

### 可选策略：
## P.S.:请根据个人喜好进行

## A.日志输出：
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j16.png">

## B.自定义应用信息：
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j17.png">
## C.32/64位部署
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j18.png">

4.Inno Setup 最终部署
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j19.png">

### 先决条件：确定你已经类似于上图那样完成结构

验证是否集成JRE/JDK库：
修改jdk的文件名，并尝试启动，出现错误说明正常：
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/Exe4j20.png">

Tips:如果你电脑本身有Java环境变量，那么这里改了文件夹名字后还是能启动。因为它会寻找你的环境变量！

5.Inno SetUp 配置：  
直接上GIF:
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/IS.gif">

最终编译出来是一个exe包，安装后就可以用了！教程结束。
<img src="http://39.105.229.249/ftp/ling/cdnpng/exe4j/end.gif">

### 参考资料
### [CSDN-No JVM ERROR](https://blog.csdn.net/qq_28114615/article/details/94402156)
### [CNBLOG-博客园](https://www.cnblogs.com/ococo/p/15875003.html)
### [CSDN-EXE4J](https://blog.csdn.net/wff900703/article/details/99960723)


#### By JDSA Ling-Ling Book Blog

---
### 声明：若要转载此文章，请注明出处，非常感谢
---