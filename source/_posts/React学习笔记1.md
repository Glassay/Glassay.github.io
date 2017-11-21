---
title: React学习笔记1
date: 2017-11-21 19:25:18
tags:
---
# React学习笔记1
## Emmet一些常用的用法
+ 子代节点: > <br>例如：div>ul>li在html中结构如下：
```html
<div>
  <ul>
    <li></li>
  </ul>
</div>
```
+ 兄弟节点：+ <br>例如：div+p+bq在html中结构如下：
```html
<div></div>
<p></p>
<blockquote></blockquote>
```
+ 父代节点：^ <br>例如：div+div>p>span+en^bq在html中结构如下：
```html
<div></div>
<div>
  <p><span></span><en></en></p>
  <blockquote></blockquote>
</div>
```
+ 重复节点：* <br>例如：ul>li*5在html中结构如下：
```html
<ul>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```
+ 成组节点：（)<br>例如：(div>dl>(dt+dd)*3)+footer>p在html中结构如下：
```html
<div>
  <dl>
    <dl></dl>
    <dd></dd>
    <dl></dl>
    <dd></dd>
    <dl></dl>
    <dd></dd>
  </dl>
</div>
<footer>
  <p></p>
</footer>
```
+ ID&ensp;#和CLASS&ensp;.节点：<br>例如：div#header+div.page+div#footer.class1.class2.class3在html中结构如下：
```html
<div id="header"></div>
<div class="page"></div>
<div id="footer" class="class1 class2 class3"></div>
```
+ 属性节点：[ ]&ensp;td[title="Hello world!" colspan=3]在html中结构如下：
```html
<td title="Hello world!" colspan="3"></td>
```


