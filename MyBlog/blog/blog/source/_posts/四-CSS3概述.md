---
title: (四)CSS3概述
date: 2022-07-08 19:41:48
tags:
- 知识
categories:
- 前端组
cover: https://tse4-mm.cn.bing.net/th/id/OIP-C.rEFlZf2xiI2BUY6BCII6QgHaEL?pid=ImgDet&rs=1
coverWidth: 730
coverHeight: 312
author: xiguayaaaaa
from:
---
(四)CSS3概述
<!--more-->

## 4.1 CSS概述

####  4.1.1 CSS 是什么

CSS全称 Cascading Style Sheets层叠样式表，是一种用来表现文件样式的计算机语言。
1.CSS不仅可以静态地修饰网页，还可以配合各种脚本语言动态地对网页各元素进行格式化。
2.CSS 能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式。
3.CSS拥有对网页对象和模型样式编辑的能力。
4.在主页制作时采用CSS技术，可以有效地对页面的布局、字体、颜色等效果实现更加精确的控制。

#### 4.1.2 CSS历史

接下来，我们从总体上看一下CSS的发展历史。

CSS 1。

1996年12月，CSS 1(Cascading Style Sheets,level 1)正式推出。在这个版本中，已经包含了font的相关属性、颜色与背景的相关属性、文字的相关属性、box的相关属性等。

CSS 2。

1998年5月，CSS 2(Cascading Style Sheets,level 2)正式推出。在这个版本中开始使用样式表结构。

CSS 2.1。

2004年2月，CSS 2.1(Cascading Style Sheets,level 2 revision 1)正式推出。它在CSS 2的基础上略微做了改动，删除了许多诸如text-shadow等不被浏览器所支持的属性。

现在所使用的CSS基本上是在1998年推出的CSS 2的基础上发展而来的。10年前在Internet刚开始普及的时候，就能够使用样式表来对网页进行视觉效果的统一编辑，确实是一件可喜的事情。但是在这10年间CSS可以说是基本上没有什么很大的变化，一直到2010年终于推出了一个全新的版本———CSS 3。

## 4.2 使用CSS能做什么

#### 4.2.1 模块与模块化结构

在CSS中，采用分工协作的模块化结构，如下表

| 模块名称                          | 功能描述                                                     |
| --------------------------------- | ------------------------------------------------------------ |
| basic box model                   | 定义各种与盒相关的样式                                       |
| Line                              | 定义各种与直线相关的样式                                     |
| Lists                             | 定义各种与列表相关的样式                                     |
| Hyperlink Presentation            | 定义各种与超链接相关的样式。訾如锚的显示方式、激活时的视觉效果等 |
| Presentation Levels               | 定义页面中元素的不同的样式级别                               |
| Speech                            | 定义各种与语音相关的样式。譬如音量、音速、说话间歇时间等属性 |
| Background and border             | 定义各种与背景和边框相关的样式                               |
| Text                              | 定义各种与文字相关的样式                                     |
| Color                             | 定义各种与颜色相关的样式                                     |
| Font                              | 定义各种与字体相关的样式                                     |
| Paged Media                       | 定义各种页眉、页脚、页数等页面元数据的样式                   |
| Cascading and inheritance         | 定义怎样对属性进行赋值                                       |
| Value and Units                   | 将页面上各种各样的值与单位进行统一定义，以供其他模块使用     |
| Image Values                      | 定义对image元素的赋值方式                                    |
| 2D Transforms                     | 在页面中实现2维空间上的变形效果                              |
| 3D Transforms                     | 在页面中实现3维空间上的变形效果                              |
| Transitions                       | 在页面中实现平滑过渡的视觉效果                               |
| Animations                        | 在页面中实现动画                                             |
| CSSOM View                        | 查看管理页面或页面的视觉效果，处理元素的位置信息             |
| Syntax                            | 定义CSS样式表的基本结构、样式表中的-一些语法细节、浏览器对于样式表的分析规则 |
| Generated and Replaced Content    | 定义怎样在元素中插入内容                                     |
| Marquee                           | 定义当一些元素的内容太大，超出了指定的元素尺寸时，是否以及怎样显示溢出部分 |
| Ruby                              | 定义页面中ruby元素（用于显示拼音文字)的样式                  |
| Writing Modes                     | 定义页面中文本数据的布局方式                                 |
| Basic User Interface              | 定义在屏幕、纸张上进行输出时页面的渲染方式                   |
| Namespaces                        | 定义使用命名空间时的语法                                     |
| Media Queries                     | 根据媒体类型来实现不同的样式                                 |
| ‘Reader’Media Type                | 定义用于屏幕阅读器之类的阅读程序时的样式                     |
| Multi-column Layout               | 在页面中使用多栏布局方式                                     |
| Template Layout                   | 在页面中使用特殊布局方式                                     |
| Flexible Box Layout               | 创建自适应浏览器窗口的流动布局或自适应字体大小的弹性布局     |
| Grid Position                     | 在页面中使用网格布局方                                       |
| Generated Content for Paged Media | 在页面中使用印刷时使用的布局方式                             |