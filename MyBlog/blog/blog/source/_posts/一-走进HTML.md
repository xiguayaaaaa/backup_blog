---
title: (一)走进HTML
date: 2022-07-08 17:04:11
tags:
- 知识
categories:
- 前端组
cover: https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.php.cn%2Fupload%2Farticle%2F000%2F000%2F029%2F5de09308e9912367.jpg&refer=http%3A%2F%2Fimg.php.cn&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1659868948&t=32927ec46d42bc175fbc4ba757b64c70
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
 走进HTML
<!--more-->
## HTML的开发环境和运行环境

HTML本质上就是一个文档，市面上常见的一些简单的文本编辑器都是可以用来开发HTML，编辑之后只需将后缀修改为".html"即可 如：记事本，EditPlus等

前端开发也有众多专业的开发软件，如：Webstrom，Sublime Text，Dreamweaver，HBuilder等，本书主要以webstrom为主要开发软件

HTML运行环境即各种浏览器，如:IE，edge，Chrome，Firefox，Safari等均可作为HTML的运行环境



## HTML文档结构

HTML文档有明确的文档结构，包含三个部分：\<HTML>中包含\<head>...\</head>部分和\<body>...\</body>部分

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
```



## Hello World

1. 创建html文件，并键入如下代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>我的第一个网页</title>
</head>
<body>
    Hello World
</body>
</html>
```



## 元素

HTML文档由HTML元素定义，一个基本元素由“开始标签”，“元素内容”，“结束标签”构成

## 块级标签和行级标签

HTML中，所有标签都是预定义的，也就是说所有的标签都有各自的特点属性，根据这些特点可将标签分为块级标签和行级标签两类

#### 块级标签

块级标签编译后在浏览器中默认没有高度，其高度由其添加的内容决定，其宽度默认为屏幕宽度，也就是说块级标签默认占一行

#### 行级标签

行级标签编译后在浏览器中默认没有宽度和高度，其宽高均有添加的内容决定，也就是说行级标签在其内容不满一行时不会换行



## HTML常用标签

#### 常用的块级标签

- 标题标签

- - 标题（Heading）通过\<h1>....\<h6>标签定义，表示一级标题至六级标题，其中\<h1>最大，\<h6>最小

  - 标题标签只用于标题

  - 标题标签不单单用于字体放大加粗，更多的是为搜索引擎使用标题帮助网页索引
  ```html
		<!DOCTYPE html>
		<html lang="en">
		<head>
		<meta charset="UTF-8">
		<title>标题标签</title>
		</head>
		<body>
		<h1>一级标题</h1>
		<h2>二级标题</h2>
		<h3>三级标题</h3>
		<h4>四级标题</h4>
		<h5>五级标题</h5>
		<h6>六级标题</h6>
		</body>
  ```

- 段落标签

- - 段落通过\<p>...\</p>标签定义，表示文档中的一个自然段
  - 注：段落标签不能嵌套使用，若想要段落标签中的内容换行显示可使用\<br/>标签换行
  ```html
	<!DOCTYPE html>
	<html lang="en">
	<head>
	<meta charset="UTF-8">
	<title>Title</title>
	</head>
	<body>
	<p>
	面朝大海，春暖花开<br/>
	作者: 海子
	</p>
	<p>从明天起，做一个幸福的人</p>
	<p>喂马，劈柴，周游世界</p>
	<p>从明天起，关心粮食和蔬菜</p>
	<p>我有一所房子，面朝大海，春暖花开</p>
	<p>从明天起，和每一个亲人通信</p>
	<p>告诉他们我的幸福</p>
	<p>那幸福的闪电告诉我的</p>
	<p>我将告诉每一个人</p>
	<p>给每一条河每一座山取一个温暖的名字</p>
	<p>陌生人，我也为你祝福</p>
	<p>愿你有一个灿烂的前程</p>
	<p>愿你有情人终成眷属</p>
	<p>愿你在尘世获得幸福</p>
	<p>我只愿面朝大海，春暖花开</p>
</body>
</html>
  
  ```

- div标签

- - div标签用于定义文档中的分区或节
  - 可以把文档分割为独立的，不同的部分
  - 在后期通过学习样式表，div可以与CSS配合对整个网页进行页面布局，模块划分，让网页制作不再有难度
  - div若不带样式单独使用则与段落标签\<p>相似，没有特定的含义

- - div若不带样式单独使用则与段落标签\<p>相似，没有特定的含义

代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无序列表</title>
</head>
<body>
    <div>
  		这是div标签，用于页面划分页面布局
  	</div>
</body>
</html>
```

- 无序列表

- - 列表可以结合链接标签用来定义新闻标题等一些较为常用的标题类链接

  - 无序列表使用\<ul>定义列表，\<li>定义列表中的条目，默认此列项目使用黑色小圆点进行标记

  - 通过在\<ul>中添加type属性更改列表的展示标记，其中disc表示实心圆，square表示矩形显示，circle表示空心圆

    代码：

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>无序列表</title>
    </head>
    <body>
        <ul>
            <li>热烈庆祝xxx同学高薪就业</li>
            <li>热烈庆祝xxx同学高薪就业</li>
        </ul>
        <ul type="square">
            <li>热烈庆祝xxx同学高薪就业</li>
            <li>热烈庆祝xxx同学高薪就业</li>
        </ul>
        <ul type="circle">
            <li>热烈庆祝xxx同学高薪就业</li>
            <li>热烈庆祝xxx同学高薪就业</li>
        </ul>
    </body>
    </html>
    ```

- 有序列表

- - 有序列表使用\<ol>定义列表，\<li>定义列表中的条目，默认此列项目使用阿拉伯数字进行标记

  - 通过在\<ol>中添加type属性更改列表的展示标记，其中‘A’表示大写字母，‘a’表示小写字母，‘I’表示大写罗马数字，‘i’表示小写罗马数字，‘1’表示阿拉伯数字（默认）

    代码：

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>有序列表</title>
    </head>
    <body>
        <h3>工作流程</h3>
        <ol>
            <li>每日晨会，任务分配</li>
            <li>工作任务</li>
            <li>工作日报</li>
            <li>下班回家</li>
        </ol>
        <ol type="A">
              <li>每日晨会，任务分配</li>
              <li>工作任务</li>
              <li>工作日报</li>
              <li>下班回家</li>
        </ol>
        <ol type="a">
              <li>每日晨会，任务分配</li>
              <li>工作任务</li>
              <li>工作日报</li>
              <li>下班回家</li>
        </ol>
        <ol type="I">
              <li>每日晨会，任务分配</li>
              <li>工作任务</li>
              <li>工作日报</li>
              <li>下班回家</li>
        </ol>
        <ol type="i">
              <li>每日晨会，任务分配</li>
              <li>工作任务</li>
              <li>工作日报</li>
              <li>下班回家</li>
         </ol>
    </body>
    </html>
    ```

- 自定义列表

- - 使用\<dl>定义列表，\<dt>定义列表中的项目，\<dd>定义列表条目

  - 自定义列表不单单只用了区分项目，后期通过样式，标签嵌套可以胜任诸多任务，如：商城，外卖类网站商品的模块划分

    代码：

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>自定义列表</title>
    </head>
    <body>
        <dl>
            <dt>pc端游戏</dt>
            <dd>穿越火线</dd>
            <dd>英雄联盟</dd>
            <dd>CSGO</dd>
            <dt>手机游戏</dt>
            <dd>和平精英</dd>
            <dd>王者荣耀</dd>
            <dd>阴阳师</dd>
        </dl>
    </body>
    </html>
    ```

- 嵌套列表

- - 列表可以通过多层嵌套实现多级列表

    代码：

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>嵌套列表</title>
    </head>
    <body>
        <ul>
            <li>茶
                <ul>
                    <li>白茶</li>
                    <li>绿茶</li>
                    <li>红茶</li>
                </ul>
            </li>
            <li>咖啡
                <ul>
                    <li>拿铁</li>
                    <li>卡布奇洛</li>
                </ul>
            </li>
        </ul>
    </body>
    </html>
    ```





#### 常用的行级标签

- 内联元素

- - 使用\<span>...\<span>表示

  - 单独使用没有特定的含义

  - 当与CSS一同使用，用来组合文档中的行内元素，如：在一行文字中给某一个字单独设置样式，再或者在某行字中添加小图标

    代码：

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>span</title>
    </head>
    <body>
        <p>
            <span style="font-size: 33px">我</span>
            最
            <span style="font-size: 33px">帅</span>
        </p>
    </body>
    </html>
    ```

- 链接标签

- - 使用\<a href="url">...\</a>表示
  - 用于从一个页面跳转到另一个页面
  - href表示跳转的链接目标
  - 默认情况下链接将以以下形式出现在网页中

- - - 在未点击访问时链接字体程蓝色并带同色下划线
    - 在点击后链接字体会程红色显示并带同色下划线

- - 标签常用属性
	![img](https://s2.loli.net/2022/07/08/q4JpNFAyeStIfE5.png)

- - 在网页开发中常用的链接有以下四种：
	![img](https://s2.loli.net/2022/07/08/SUz5vErMnaX4HFx.png)

附：

空链接“#”与“javascript:void(0)”的区别：

1. “#”包含一个位置信息，默认为网页顶端，当页面高度大于一屏时，点击后会跳转到网页顶部
2. “javascript:void(0)”是一个伪协议，表示url内容通过javascript执行，而void(0)则表示不作任何操作，这样该标签既保留了链接样式还能防止页面跳转
3. 空链接通常通过添加javascript事件去做一些其它操作，如：设置收藏，设置首页，弹窗等，这些会在本书javascript事件章节详细讲解

附：

绝对路径和相对路径

绝对路径：是指文件在硬盘上的真正存在的路径，如：一张名为“头像.jpg”的图片或一个名为“index.html”的网页存放在我计算机中的“C:\Users\document\WebstormProjects\untitled15”目录中，则图片的绝对路径为“C:\Users\document\WebstormProjects\untitled15\头像.jpg”，网页的绝对路径为“C:\Users\document\WebstormProjects\untitled15\index.html”，但在开发时很少使用绝对路径，当指定了决定路径后在项目路径在本地计算机上是没问题的，但上传到服务器或在其它计算机上时很可能会出现找不到路径，路径错误等问题。

相对路径：指由文件本身相对于目标文件的路径，使用相对路径的三种写法，下边以网页index.html引用网页Login.html为例说明：

1.若Login.html相对index.html是在同一目录，那么网页在引用图片时则只需要通过Login.html名称+后缀引用即可

2.若网页Login.html存在某个文件夹中，文件夹与网页index.html属于同一目录，那么网页index.html在引用网页Login.html时则需要通过找到文件夹使用分隔符“/”才能找到文件夹中相对的网页Login.html文件，这里需要注意：绝对路径使用分隔符“\”，相对路径使用分隔符“/”

3.若网页index.html和网页Login.html都存在不同的文件夹中，两个不同的文件夹属于同一目录，那么网页index.html在引用网页Login.html时则需要通过“../”返回上一级路径再去引用存放网页Login.html的文件夹再使用分隔符“/”引用网页Login.html，这里需要注意一个“../”，表示网上返回一级，如果要返回多个则需要使用多个“../”

```

锚链接示例代码：
	```html
	<!DOCTYPE html>
	<html lang="en">
	<head>
	<meta charset="UTF-8">
	<title>Title</title>
	</head>
	<body>
	<a id="top">这是网页顶部</a>
	<a href="#middle">跳转至网页中部</a>
    <a href="#bottom">跳转至网页底部</a>
    <p>网页内容</p>
    <p>....</p>
    <p>这里省略若干行相同内容</p>
    <a id="middle">这是网页中部</a>
    <a href="#top">跳转至网页顶部</a>
    <a href="#bottom">跳转至网页底部</a>
    <p>网页内容</p>
    <p>....</p>
    <p>这里省略若干行相同内容</p>
    <a href="#middle">跳转至网页中部</a>
    <a href="#top">跳转至网页顶部</a>
    <a id="bottom">这是网页底部</a>
</body>
</html>
```
附：
1. 锚链接是在页面内的不同位置跳转，本质上就是元素间的跳转
2. 使用锚链接首先要建立锚点目标，只需要给元素添加id或name属性即可 如：\<a name="top">,\<div id="top">
3. 建立好锚点目标后再使用\<a href="#id值或name值">引用锚点
4. 如果不同页面跳转，同时存在锚点，则先跳转到要跳转的页面，然后在寻找锚点元素进行跳转



```html
		<!DOCTYPE html>
		<html lang="en">
		<head>
		<meta charset="UTF-8">
		<title>首页</title>
		</head>
		<body>
			<a href="demo.html#bottom">走你</a>
		</body>
		</html>
		<!DOCTYPE html>
		<html lang="en">
		<head>
		<meta charset="UTF-8">
		<title>测试页</title>
		</head>
		<body>
			<p>这是内容</p>
			<p>.....</p>
			<p>此时省略若干行相同内容</p>
			<p>这是内容</p>
			<div id="bottom"></div>
		</body>
		</html>
```


- 图片标签

- - 图片标签使用\<img/>表示，图片标签没有结束标签“/”表示结束
  - 标签属性
  	![img](https://s2.loli.net/2022/07/08/YRABTNJk15doKQi.png)

  代码：

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>图片标签</title>
  </head>
  <body>
      <img src="F.jpg" alt="这是替换文本" title="这是一张图片" width="600" height="406">
  </body>
  </html>
  ```
```



- 图片增强（map）

- - \<map>标签有助于定义图像映射。图像映射指的是图像中包含一个或多个可点击区域。\<map>标签与\<area>标签一起确定可点击区域。可点击区域可以是矩形、圆形或多边形区域这些形状之一。如果不指定形状，就会认为是整个图像

    示例

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>
    </head>
    <body>
        <div>
            <img src="../images/mapImages/4.png" width="592" height="182" alt="mapSelect" usemap="#circusmap">
            <map name="circusmap">
                <area shape="rect" coords="82,70,155,133" href="map2.html">
                <area shape="rect" coords="297,70,387, 133" href="map1.html">
                <area shape="rect" coords="480,70,572, 133" href="map3.html">
            </map>
        </div>
    </body>
    </html>
```


知识补充：

- \<area>标签定义图像映射中的区域

  ​	shape属性 

  ​     		shape属性用于定义图像映射中对鼠标敏感的区域的形状

  ​					圆形（circ或circle）

  ​					多边形（poly或polygon）

  ​					矩形（rect或rectangle）

  ​	coords属性

  ​					圆形：shape="circle"，coords="x,y,z"

  ​					这里的 x 和 y 定义了圆心的位置（"0,0" 是图像左上角的坐标），z 是以像素为单位的圆形半径。

  ​					多边形：shape="polygon"，coords="x1,y1,x2,y2,x3,y3,..."

  ​					每一对 "x,y" 坐标都定义了多边形的一个顶点（"0,0" 是图像左上角的坐标）。定义三角形至少需要三组坐标；高纬多边形则需要更多数量的顶点。

  ​					多边形会自动封闭，因此在列表的结尾不需要重复第一个坐标来闭合整个区域。

  ​					矩形：shape="rectangle"，coords="x1,y1,x2,y2"

  ​					第一个坐标是矩形的一个角的顶点坐标，另一对坐标是对角的顶点坐标，"0,0" 是图像左上角的坐标。请注意，定义矩形实际上是定义带有四个顶点的多边形的一种简化方法。

- 常用文本格式化标签
  ![img](https://s2.loli.net/2022/07/08/obBW4smqSA1EpVL.png)

  代码：
  ```html
  <!DOCTYPE HTML>
  <head>
  <meta charset="utf-8">
  </head>
  <body>
  <b>定义粗体文本</b>
  <br/>
  <em>定义着重文字</em>
  <br/>
  <i>定义斜体文字</i>
    <br/>
  <small>定义小号文字</small>
  <br/>
  <strong>定义加重语气</strong>
  <br/>
  定义下标字 <sub>aa</sub>
  <br/>
  定义上标字 <sup>aa</sup>
  <br/>
  <ins>定义插入字(加了下划线)</ins>
  <br/>
  <del>定义删除字(加了删除线)</del>
  </body>
  ```
