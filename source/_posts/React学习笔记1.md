---
title: React学习笔记1
date: 2017-11-21 19:25:18
tags:
---
# React学习笔记1
## Emmet一些常用的用法
* 子代节点: > &ensp; 例如：div>ul>li&ensp; 在html中结构如下：
```html
<div>
  <ul>
    <li></li>
  </ul>
</div>
```
* 兄弟节点：+ &ensp; 例如：div+p+bq&ensp; 在html中结构如下：
```html
<div></div>
<p></p>
<blockquote></blockquote>
```
* 父代节点：^ &ensp; 例如：div+div>p>span+en^bq&ensp; 在html中结构如下：
```html
<div></div>
<div>
  <p><span></span><en></en></p>
  <blockquote></blockquote>
</div>
```

