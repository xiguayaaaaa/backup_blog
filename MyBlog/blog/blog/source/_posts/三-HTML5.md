---
title: (三)HTML5
date: 2022-07-08 19:36:10
tags:
- 知识
categories:
- 前端组
cover: https://ts1.cn.mm.bing.net/th/id/R-C.fa4b93dc580e788f183ae3a6793bfe56?rik=huVHqQFEczu30g&riu=http%3a%2f%2fnews.mydrivers.com%2fImg%2f20110119%2fS08534319.png&ehk=isp2A3sdx7Wt%2fOngckZQfXLnIXcAbie9gvxAVg%2fRt%2bA%3d&risl=&pid=ImgRaw&r=0&sres=1&sresct=1
coverWidth: 550
coverHeight: 275
author: xiguayaaaaa
from:
---

 (三)HTML5
 <!--more-->
## 3.1新增元素

#### 3.1.1 新增的结构元素

- \<section>元素

\<section>元素表示页面中的内容区块，如：页眉，页脚，章节等部分

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>section</title> 
</head>
<body>
  <section>
    <h1>区域一</h1>
    <p>这里是区域一的内容</p>
  </section>

  <section>
   <h1>区域二</h1>
    <p>这里是区域二的内容</p>
  </section>
</body>
</html>
```

- \<article>元素

\<article>元素表示页面中的一块与上下文不相关的独立内容，如：新闻页中诸多文章中的某篇文章

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>article</title> 
</head>
<body>

  <article>
    <h1>两个“万岁”</h1>
    <p>“伟大、光荣、正确的中国共产党万岁！”</p>
		<p>“伟大、光荣、英雄的中国人民万岁！”</p>
  </article>
</body>
</html>
```

- \<aside>元素

\<aside>表示\<article>元素的内容之外的，它的内容应该与附近内容相关

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>aside</title> 
</head>
<body>

  <p>神州十二号飞船成功升空</p>

  <aside>
    <h4>飞船抵达中国空间站</h4>
    <p>6月19日上午，神舟十二号飞船抵达距离天和核心舱200米的停留点，开始进行对接准备。
      通过使用最先进的快速交会对接自动化技术
      这一切都要归功于从一次次太空飞行中总结的的经验。</p>
  </aside>

</body>
</html>
```

- \<header>元素

\<header>元素表示页面中的一个内容块或整个页面的标题

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>header</title> 
</head>
<body>
  <article>
    <header>
      <h1>飞船抵达中国空间站</h1>
    </header>
    <p>
      6月19日上午，神舟十二号飞船抵达距离天和核心舱200米的停留点，开始进行对接准备。
      通过使用最先进的快速交会对接自动化技术
      这一切都要归功于从一次次太空飞行中总结的的经验。
    </p>
  </article>
</body>
</html>
```

- \<footer>元素

\<footer>元素表示整个页面或页面中一个区域内的脚注，一般包含作者的基本信息

代码：

```html
<!DOCTYPE html>
<html>
<head> 
    <meta charset="UTF-8">
    <title>header</title> 
</head>
<body>
    <article>
        <header>
            <h1>飞船抵达中国空间站</h1>
        </header>
        <p>
            6月19日上午，神舟十二号飞船抵达距离天和核心舱200米的停留点，开始进行对接准备。
            通过使用最先进的快速交会对接自动化技术
            这一切都要归功于从一次次太空飞行中总结的的经验。
        </p>
    </article>
    <footer>
        <p>&copy;环球网</p>
      	<p>发表时间：7-12</p>
    </footer>
</body>
</html>
```

- \<nav>元素

\<nav>元素通常在内嵌套\<a>标签表示页面的导航链接部分

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>nav</title> 
</head>
<body>

  <nav>
    <a href="/html/">HTML</a> |
    <a href="/css/">CSS</a> |
    <a href="/js/">JavaScript</a> |
    <a href="/jquery/">jQuery</a>
  </nav>

</body>
</html>
```

- \<video>元素

- - \<video>元素用来插入视频
  - \<video>元素仅支持MP4，WebM，Ogg视频格式
  - 元素属性表：

| 属性                                                         | 值               | 描述                                                         |
| ------------------------------------------------------------ | ---------------- | ------------------------------------------------------------ |
| [autoplay](https://www.runoob.com/tags/att-video-autoplay.html) | autoplay         | 如果出现该属性，则视频在就绪后马上播放。                     |
| [controls](https://www.runoob.com/tags/att-video-controls.html) | controls         | 如果出现该属性，则向用户显示控件，比如播放按钮。             |
| [height](https://www.runoob.com/tags/att-video-height.html)  | pixels           | 设置视频播放器的高度。                                       |
| [loop](https://www.runoob.com/tags/att-video-loop.html)      | loop             | 如果出现该属性，则当媒介文件完成播放后再次开始播放。         |
| [muted](https://www.runoob.com/tags/att-video-muted.html)    | muted            | 如果出现该属性，视频的音频输出为静音。                       |
| [poster](https://www.runoob.com/tags/att-video-poster.html)  | URL              | 规定视频正在下载时显示的图像，直到用户点击播放按钮。         |
| [preload](https://www.runoob.com/tags/att-video-preload.html) | autometadatanone | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
| [src](https://www.runoob.com/tags/att-video-src.html)        | URL              | 要播放的视频的 URL。                                         |
| [width](https://www.runoob.com/tags/att-video-width.html)    | pixels           | 设置视频播放器的宽度。                                       |

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>video</title> 
</head>
<body>

  <video width="320" height="240" controls>
    <source src="movie.mp4"  type="video/mp4">
    <source src="movie.ogg"  type="video/ogg">
    您的浏览器不支持 HTML5 video 标签。
  </video>

</body>
</html>
```

- \<audio>元素

- - \<audio>元素用来插入音频
  - \<audio>元素仅支持Ogg和MP3格式
  - 元素属性表

| 属性                                                         | 值               | 描述                                                        |
| ------------------------------------------------------------ | ---------------- | ----------------------------------------------------------- |
| [autoplay](https://www.runoob.com/tags/att-audio-autoplay.html) | autoplay         | 如果出现该属性，则音频在就绪后马上播放。                    |
| [controls](https://www.runoob.com/tags/att-audio-controls.html) | controls         | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
| [loop](https://www.runoob.com/tags/att-audio-loop.html)      | loop             | 如果出现该属性，则每当音频结束时重新开始播放。              |
| [muted](https://www.runoob.com/tags/att-audio-muted.html)    | muted            | 如果出现该属性，则音频输出为静音。                          |
| [preload](https://www.runoob.com/tags/att-audio-preload.html) | autometadatanone | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
| [src](https://www.runoob.com/tags/att-audio-src.html)        | *URL*            | 规定音频文件的 URL。                                        |

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>audio</title> 
</head>
<body>
  <audio controls>
    <source src="music.ogg" type="audio/ogg">
    <source src="music.mp3" type="audio/mpeg">
  您的浏览器不支持 audio 元素。
  </audio>
</body>
</html>
```

- \<mark>元素

\<mark>元素主要用来在视觉上向用户呈现哪些需要突出显示或高亮显示的文字，一般用在搜索结果中向用户高亮显示搜索关键词

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>mark</title> 
</head>
<body>
  <p>神舟十二号航天员乘组圆满完成空间站阶段<mark>首次出舱</mark>活动全部既定任务</p>
</body>
</html>
```

- \<ruby>元素

\<ruby>表示中文注音或字符

- \<rt>元素

\<rt>元素与\<ruby>配合使用用来解释或发音

- \<rp>元素

\<rp>元素与\<ruby>一起使用，以定义不支持\<ruby>元素的浏览器显示内容，以括号的形式出现如：汉字(Han Zi)

代码：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>ruby,rt,rp
  </title> 
</head>
<body>

<ruby>
  汉 <rp>(</rp><rt>Han</rt><rp>)</rp>
  字 <rp>(</rp><rt>zi</rt><rp>)</rp>
</ruby>

</body>
</html>
```

- \<details>元素

<details>元素表示用户要求得到的细节信息，与<summary>配合使用，<summary>提供标题或图例，用户点击标题时，会显示户细节信息，<summary>元素应该是<details>元素的第一个元素

代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>details</title>
</head>
<body>
    <details>
        <summary>空间站</summary>
        空间站（space station）又称太空站、航天站。
      	是一种在近地轨道长时间运行、可供多名航天员巡访、长期工作和生活的载人航天器。
      	空间站分为单模块空间站和多模块空间站两种。
      	单模块空间站可由航天运载器一次发射入轨，多模块空间站则由航天运载器分批将各模块送入轨道，在太空中将各模块组装而成。
      	在空间站中要有人能够生活的一切设施，空间站不具备返回地球的能力。
    </details>
</body>
</html>
```

## 3.2 全局属性

#### 3.2.1 contentEditable属性

contentEditable属性由微软开发并被其它浏览器反编译投入引用的一个全局属性，该属性允许用户编辑元素内容，该属性是一个布尔值的属性，可以被指定false或true

该属性默认inherit（继承）状态，属性为true时，元素被指定为允许编辑；属性为false时，元素被指定为不允许编辑状态；未指定值时，则由inherit状态决定，如果父元素是可编辑元素，则该元素也可编辑

在编辑完成后，如果想要保存其中的内容，只能把该元素的innerHTML发送到服务器端进行保存，目前还没有特别的API来保存编辑后的元素内容

代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>contenteditable</title>
</head>
<body>
    <ul contenteditable="true">
        <li>这是预编译内容</li>
        <li>这是预编译内容</li>
        <li>这是预编译内容</li>
    </ul>
</body>
</html>
```

运行结果：

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1626161477737-77ec780f-ee67-4db7-aeff-ab2ff54b335d.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_19%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

#### 3.2.2 designMode属性

designModel属性用来指定整个页面是否可编辑，当页面可编辑时，页面中任何支持contenteditable属性的元素都变成可编辑状态。该属性只能在JavaScript脚本里被编辑修改，该属性有两个值 “on”或“off”，当属性被指定为“on”时，页面为可编辑状态，为“off”时，页面不可编辑

代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>designMode</title>
    <script>
        document.designMode="on";
    </script>
</head>
<body>
    <ul>
        <li>这是原有内容</li>
        <li>这是原有内容</li>
        <li>这是原有内容</li>
    </ul>
    <a href="javascript:void(0)">链接</a>
</body>
</html>
```

运行结果：

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1626162780404-4163f601-90ab-4986-abdd-5843a5cf39b4.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

#### 3.2.3 hidden属性

在HTML 5中，所有的元素都允许使用一个hidden属性。该属性类似于input元素中的 hidden元素，功能是通知浏览器不渲染该元素。使该元素处干不可见状态。但是元素中的内容还是浏览器创建的，也就是说页面装载后允许使用JavaScript脚本将该属性取消，取消后该元素变为可见状态，同时元素中的内容也即时显示出来。Hidden属性是一个布尔值的属性。当设为true时，元素处于不可见状态;当设为false时，元素处于可见状态