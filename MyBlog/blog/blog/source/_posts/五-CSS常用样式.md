---
title: (五)CSS常用样式
date: 2022-07-08 19:42:18
tags:
- 知识
categories:
- 前端组
cover: https://www.codesnail.com/wp-content/uploads/2021/02/css-syntax-structure.png
coverWidth: 1280
coverHeight: 650
author: xiguayaaaaa
from:
---
(五)CSS常用样式
<!--more-->
## 5.3 CSS 常用样式属性

#### 5.3.1宽高

- - 宽width：像素值/百分比（上一级标签的百分之多少）
  - 高height：像素值/百分比（上一级标签的百分之多少[注：当标签为body下的第一层标签时，高度使用百分比是不生效的]）
  - 示例

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630404127941-15c52bda-471e-4f8f-badd-94657b35432f.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_17%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630404138115-693d3125-52b8-4fdc-b468-ab6f777ba28c.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630404170319-5ab39ea2-c836-4221-9f15-35afbf841664.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_19%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |

#### 5.3.2文字

- - 文字大小

- - - font-size：像素值

- - 文字颜色

- - - color:颜色单词/十六进制值/rgba值

- - 文字对齐方式

- - - text-align:居中/靠左/靠右

- - 文字的字体设置

- - - font-family:字体

示例

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630404233490-92063cc0-c11a-41ea-8787-37e5c94c2d40.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_24%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

#### 5.3.3浮动

- - 标准文档流

- - - web页面的制作不同于设计软件，它是个流，必须从上而下，先执行渲染显示上边的元素，依次向下渲染显示
    - 我们知道元素分块级和行级元素两类，如果页面完全遵循文档流去开发就会导致很多页面排版不能实现或不能完全实现
    - 通过浮动我们可以让元素脱离标准流，实现块级元素并排等一些效果

- - 浮动特点

- - - 脱离标准流
    - 元素并排（如果容器宽度足够元素则在容器宽度范围内并排，如果宽度不够则容器内元素会依次换行排列）
    - 收缩（如果一个没有设置宽度的元素浮动，那么元素的宽度会自动收缩为内容宽度）

- - 注：在学习初期关于浮动要遵循的一个原则：**不要让一个元素单独浮动，要浮一起浮，要么都别浮**
  - 浮动属性

- - - 左浮动    float:left;
    - 右浮动    float:right

脱标示例

| 代码                                                         | 运行结果                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <!DOCTYPE html><html lang=**"en"**><head>  <meta charset=**"UTF-8"**>  <title>**Title**</title>  <style>    .box{        width: 300**px**;        height: 300**px**;        background-color: **red**;             }      .FBox{        width: 450**px**;        height: 450**px**;        background-color: **aqua**;      }    </style></head><body>  <div class=**"box"**></div>  <div class=**"FBox"**></div></body></html> | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630411052874-f74c9cef-be0c-4eb3-8305-7009f53bf4fa.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_15%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| <!DOCTYPE html><html lang=**"en"**><head>  <meta charset=**"UTF-8"**>  <title>**Title**</title>  <style>    .box{        width: 300**px**;        height: 300**px**;        background-color: **red**;        float: **left**;      }      .FBox{        width: 450**px**;        height: 450**px**;        background-color: **aqua**;      }    </style></head><body>  <div class=**"box"**></div>  <div class=**"FBox"**></div></body></html> | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630411089649-7e53a85f-5dec-427a-b4e5-f561b68a2fc9.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

收缩示例

| 代码                                                         | 示例                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <!DOCTYPE html><html lang=**"en"**><head>  <meta charset=**"UTF-8"**>  <title>**Title**</title>  <style>    .box{        background-color: **red**;       }    </style></head><body>  <div class=**"box"**>**这是一行字**</div></body></html> | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630411191956-d9627364-0284-47bd-92c4-cd34f74deffa.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_23%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| <!DOCTYPE html><html lang=**"en"**><head>  <meta charset=**"UTF-8"**>  <title>**Title**</title>  <style>    .box{        background-color: **red**;        float: **left**;      }     </style></head><body>  <div class=**"box"**>**这是一行字**</div></body></html> | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630411233384-6aaacf3c-b4ed-49a6-a17f-da47de55c0fa.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

左浮动示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            background-color: red;
            float: left;
        }
    </style>
</head>
<body>
    <div class="box">这是第一行字</div>
    <div class="box">这是第二行字</div>
    <div class="box">这是第三行字</div>
    <div class="box">这是第四行字</div>
</body>
</html>
```

右浮动示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            background-color: red;
            float: right;
        }
    </style>
</head>
<body>
    <div class="box">这是第一行字</div>
    <div class="box">这是第二行字</div>
    <div class="box">这是第三行字</div>
    <div class="box">这是第四行字</div>
</body>
</html>
```

#### 5.3.4背景

- - 背景图 background-image:url("图片地址")

- - - 注：

- - - - 在元素添加背景图时其运行时高度必须大于1
      - 背景图处于元素的最底层不会占用元素内容的存储空间

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100%;
            height: 200px;
            background-image: url("../images/mapImages/4.png");
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

- - 背景图大小 background-size:宽度 高度；

- - - 注：

- - - - 为背景图设置大小时需要注意该图的纵横比（容易出现背景变形）

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100%;
            height: 200px;
            background-image: url("../images/mapImages/1.png");
            background-size: 100% 100%;
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

- - 背景重复 background-repeat:no-repeat/repeat-x;repeat-y;

- - - 当图片宽高小于容器宽高时图片默认会铺满整个容器，会导致背景重复
    - 背景重复属性值默认为repeat（重复），也可以设置为

- - - - no-repeat:不重复
      - repeat-x：X轴重复
      - repeat-y：Y轴重复

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100%;
            height: 200px;
            background-image: url("../images/mapImages/1.png");
            /*background-repeat: repeat-x;*/
            /*background-repeat: repeat-y;*/
            background-repeat: no-repeat;
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

- - 背景位移 background-position:x轴值 Y轴值；

- - - 当背景图大小小于容器大小的时候，容器中添加背景图后只能展示出部分背景图
    - 通过背景位移，可以移动背景图片让容器中显示背景图中想要展示分部分
    - 注：

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630463229523-5d0c94e2-3a53-4b6a-a6ba-5e109ae8913c.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100px;
            height: 100px;
            background-image: url("../images/mapImages/4.png");
            background-repeat: no-repeat;
            border: 1px solid black;
            background-position: -56px -30px;
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

- - 背景色 background-color:颜色单词/十六进制值/rgba值

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100%;
            height: 200px;
            background-color: red;
            /*background-color: #ff0000;*/
            /*background-color: rgba(255, 0, 0, 0.71);*/
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

- - 背景渐变

示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100%;
            height: 200px;
            background:linear-gradient(#ff0000,#ffffff);
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

#### 5.3.5阴影 box-shadow

- - 语法：

box-shadow: h-shadow v-shadow blur spread color inset;

- - 属性值：

| 值       | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| h-shadow | 必需的。水平阴影的位置。允许负值                             |
| v-shadow | 必需的。垂直阴影的位置。允许负值                             |
| blur     | 可选。模糊距离                                               |
| spread   | 可选。阴影的大小                                             |
| color    | 可选。阴影的颜色。在[CSS颜色值](https://www.runoob.com/cssref/css_colors_legal.aspx)寻找颜色值的完整列表 |
| inset    | 可选。从外层的阴影（开始时）改变阴影内侧阴影                 |

示例一

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100px;
            height: 100px;
            background-color: white;
            box-shadow: 0px 0px 50px 2px gainsboro;
        }
    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

示例二

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .demo{
            width: 100px;
            height: 100px;
            background-color: white;
            box-shadow:    0px -10px 0px 0px #ff0000,   /*上边阴影  红色*/
            -10px 0px 0px 0px #3bee17,   /*左边阴影  绿色*/
            10px 0px 0px 0px #2279ee,    /*右边阴影  蓝色*/
            0px 10px 0px 0px #eede15;    /*下边阴影  黄色*/
            border-radius: 50%;
        }

    </style>
</head>
<body>
    <div class="demo"></div>
</body>
</html>
```

#### 5.3.6圆角 border-[*-*-]radius:圆角值

圆形示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: red;
            border-radius: 50%;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```

单角示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: red;
            border-bottom-left-radius: 20px;
            /*border-bottom-right-radius: 20px;*/
            /*border-top-right-radius: 20px;*/
            /*border-top-left-radius: 20px;*/
            
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```