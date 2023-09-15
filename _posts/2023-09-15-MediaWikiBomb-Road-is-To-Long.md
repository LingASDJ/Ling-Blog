---
layout: post
title:  辉梦Wiki后端数据爆炸,Wiki的道路还有很长.....
tags: [九月随笔,搭建Wiki,辉梦工作室]
author: JDSALing
stickie: true
---

---
撰写于2023年9月14日--建议阅读时间：10分钟

---

已经很久没有更新博客了,主要是真的很忙.  
近期和朋友正在搭建Wiki站点来让我的mod丰富.  
记录一些事情来进行一个九月随笔.

# 1.辉梦Wiki的诞生
我在近期与一位在PD群认识的新朋友(QinYue)一起合作,  
在某一天的早上,我提出了MediaWiki建站想法.  
我们一拍即合,9.12号,辉梦Wiki-Demo版本正式上线.

# 2.灾难前的宁静
在研究MediaWiki的道路上,我发现它并没有如此的简单.  
无论是模板,导入外部JS,CSS等,都是一个未知的挑战.  
我在进行这些的探索之路上,也发现了一些技巧.  
目前,在我看来,最有用的无疑是"模板"系统,它可以很省时省力.
以下是我构建的一个模板例子

```html
<table class="wikitable itemInfo" style="text-align:center;width:auto;display: table;white-space: normal;">
    <tr>
    <td class="nomobile" colspan="2" style="color:white; font-weight:bold; background-color:{{{item_color}}}">{{{item_title}}}
    </td></tr>
    <tr>
    <td class="nomobile" rowspan="6" width="28%">[[File:{{{item_image}}}]]</td>
    <th class="nomobile">物品类型:{{{item_type}}}
    </th></tr>
    <tr>
    <td class="nomobile">{{{item_desc}}}
    </td>
    </tr>
    <tr>
    <th class="nomobile">{{{item_type}}}数据</th>
    </tr>
<tr>
    <td class="nomobile">{{{item_alter}}}
    </td></tr>
</table>
```

在使用的时候只需要与之一一对应即可: 

```html
PD物品框架|item_color=#ff0000|item_title=嗜血荆棘-T6|item_image=BloodCite.png|item_desc=鲜血腐蚀所残留的倒悬树之刺。舍弃了仅存的秩序，独留狂暴与混乱。

攻击时有概率给敌人施加<font color=#ff0000>流血和恐惧</font>效果。
特性：升级机制与蓄血圣杯相同。

+3前攻击将概率流失自身2点生命值并刺伤自己。

+5时取消负面影响，攻击距离+1，+20%精准。

+10时每次有效攻击将有大概率汲取一定生命力回馈给自身

这是一把十分精准的武器

一般情况下这件6阶近战武器可以造成2~6点伤害，
并且需要14点力量来正常使用.|item_type=近战武器|item_alter=基础力量:10 基础伤害:2-6 攻速:普通 攻距:详见描述
<font color="blue">注：该物品不能自动生成，属于合成类武器</font>

有关于此物品的合成参考，请参考此武器的合成表
```

同时,我也在参考类似于`PRTS`这样的MediaWiki进行学习....

# 3.辉梦Wiki第一代的末路
9.14,我仍然在进行页面维护与调整,  
我为辉梦添加了更多有用的插件,   
但是,在添加完一个叫`Nuke`批量删除插件后,  
我删除了大量的页面,
这直接导致了部分页面PHP报错,  
加上MediaWiki的数据无法在数据库中找到,  
经朋友和我一致决定,重新安装MediaWiki.  
至此,辉梦第一代运行享年3天,宣告结束.

# 4.Wiki的道路还有很长

<font color="#008688">路漫漫其修远兮，吾将上下而求索</font>

对于MediaWiki,  
由于我不熟练和对插件的过度使用终究酿成大祸.  
但人又哪有没有跌倒的时候?  
哪里跌倒,就在哪里爬起来.  
人就是这样一步一步进步的.  
吸取教训,V2辉梦会更好!

#### By JDSA Ling-Ling Book Blog


