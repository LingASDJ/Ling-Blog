---
layout: page
title: 友情链接
tagline: 旅途中总会遇到志同道合的朋友！
permalink: /links.html
---

---

{% for f in site.data.friends %}
<div class="link-chip-div"><a href="{{f.url}}" target="_blank" class="link-chip ripple">
 <img alt="{{f.describe}}" src="{{f.image}}" class="link-chip-icon"/>
 {% if f.skin %}<img style="filter:opacity(0.8);float:right;height:64px;margin-right:-8px" src="{{f.skin}}" />{% endif %}
 <span title="{{f.describe}}" class="link-chip-title">{{f.name}}</span>
 <p class="link-chip-dc">{{f.describe}}</p></a></div>
{% endfor %}

<hr/>

  {% if site.data.social.valine_comment.enable  == true %}
  <script src="/comment/av-min.js"></script>
  <script src="/comment/Valine.min.js"></script>
  <div id="comments"></div>
  {% include comments.html %}
  {% endif %}
  {% include scripts.html %}

### AnsdoShip Web Page
AnsdoShip--[**[AnsdoShip]**](https://ansdoship.github.io/)

---

### 秦月的外交部
诺瑟斯外交部--[**[QinYue-Blog]**](http://www.qinyueqwq.top/)

---

### Link's Blog
Link的Blog--[**[Link-Blog]**](https://atlinker.cn/)

---
### Steveubuntu's Blog
Steveubuntu--[**[Steveubuntu]**](https://blog.stevesuk-official.ml/)

### LiuLiu's Blog
LiuLiu的Blog--[**[LiuLiu-Blog]**](https://liusxs.github.io/liuliu/)

### Mason's Blog
Mason的Blog--[**[Mason-Blog]**](https://mason369.github.io/Mason_blog/)

### Tmaize's Blog
Tmaize的Blog--[**[Tmaize-Blog]**](https://blog.tmaize.net/)

---
### Cold Mint
Cold Mint--[**[ColdMint-Blog]**](https://coldmint.top/)

---
### Tianscar
碳酸天剑的Blog--[**[Tianscacr-Blog]**](https://blog.tianscar.com)  
碳酸天剑的网址导航--[**[Tianscacr-SiteNav]**](https://sitenav.tianscar.com)

---
### Prohonor
Prohonor--[**[Progressive Tune]**](https://progressive-tune.github.io/ptr/)  

---