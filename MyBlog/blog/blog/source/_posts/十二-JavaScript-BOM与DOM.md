---
title: (十二)JavaScript BOM与DOM
date: 2022-07-08 20:50:16
tags:
- 知识
categories:
- 前端组
cover: https://tse3-mm.cn.bing.net/th/id/OIP-C.W1LAyJAcbJobV0FBqPu-wwHaD4?pid=ImgDet&rs=1
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
(十二)JavaScript BOM与DOM
<!--more-->

# 第十二章 JavaScript BOM与DOM

## BOM（borwser object Model）

#### 浏览器对象模型

- - 使用对象描述浏览器的各个部分
  - BOM提供与浏览器窗口交互的对象
  - BOM主要用于管理窗口与窗口之间的通讯，所以核心对象是窗口（window）

- BOM里有什么

- - 图示

    ![img](https://files.catbox.moe/ccpeyl.png)

- - 与浏览器进行交互的一些对象

- - - 移动，调整浏览器大小的window对象
    - 用于导航的location对象history
    - 获取浏览器，用户屏幕信息的navigator与screen对象

##### window对象

- - open()方法用于打开一个新窗口或查找一个窗口
- - - 语法
    - window.open(url,name,feature,replace)

| 参数    | 描述                                                         |
| ------- | ------------------------------------------------------------ |
| url     | 声明要在新窗口中显示文档的url                                |
| name    | 该字符声明了新窗口的名称。这个名称可以用作标记 和的属性 target 的值。如果该参数指定了一个已经存在的窗口，那么 open() 方法就不再创建一个新窗口，而只是返回对指定窗口的引用。在这种情况下，features 将被忽略。 |
| feature | 声明了新窗口要显示的标准浏览器的特征                         |
| replace | 一个可选的布尔值。规定了装载到窗口的 URL 是在窗口的浏览历史中创建一个新条目，还是替换浏览历史中的当前条目。支持下面的值：true - URL 替换浏览历史中的当前条目。false - URL 在浏览历史中创建新的条目。 |

- 案例 打开新窗口控制其外观样式

  ![img](https://files.catbox.moe/9cmg9b.png)

- 窗口特征表

| channelmode=yes\|no\|1\|0 | 是否使用剧院模式显示窗口。默认为 no。                        |
| ------------------------- | ------------------------------------------------------------ |
| directories=yes\|no\|1\|0 | 是否添加目录按钮。默认为 yes。                               |
| fullscreen=yes\|no\|1\|0  | 是否使用全屏模式显示浏览器。默认是 no。处于全屏模式的窗口必须同时处于剧院模式。 |
| height=pixels             | 窗口文档显示区的高度。以像素计。                             |
| left=pixels               | 窗口的 x 坐标。以像素计。                                    |
| location=yes\|no\|1\|0    | 是否显示地址字段。默认是 yes。                               |
| menubar=yes\|no\|1\|0     | 是否显示菜单栏。默认是 yes。                                 |
| resizable=yes\|no\|1\|0   | 窗口是否可调节尺寸。默认是 yes。                             |
| scrollbars=yes\|no\|1\|0  | 是否显示滚动条。默认是 yes。                                 |
| status=yes\|no\|1\|0      | 是否添加状态栏。默认是 yes。                                 |
| titlebar=yes\|no\|1\|0    | 是否显示标题栏。默认是 yes。                                 |
| toolbar=yes\|no\|1\|0     | 是否显示浏览器的工具栏。默认是 yes。                         |
| top=pixels                | 窗口的 y 坐标。                                              |
| width=pixels              | 窗口的文档显示区的宽度。以像素计。                           |

- setInterval()每隔指定的毫秒运行指定的代码/函数

- 案例

  ![img](https://files.catbox.moe/gezs9p.png)

- setTimeout()经过指定毫秒数运行一次指定的代码/函数

- 案例

  ![img](https://files.catbox.moe/r0dclo.png)

- location地址栏对象

- - href：设置或获取整个URL为字符串

- 案例

  ![img](https://files.catbox.moe/rk4u5p.png)

- reload()：重新加载

- replace():用新文档替换当前文档

- 案例

  ![img](https://files.catbox.moe/e2r3lh.png)

##### 屏幕对象（Screen）用来获取电脑屏幕的一些数据

- - availHeight：获取系统屏幕的工作区高度（浏览器的页面高度）

- - 案例

    ![img](https://files.catbox.moe/k600si.png)

- availWidth：获取系统屏幕的工作区宽度（浏览器页面宽度）

- height：获取屏幕的垂直分辨率

- width：获取屏幕的水平分辨率

- - 案例

    ![img](https://files.catbox.moe/oxiqgh.png)

## DOM编程

#### 文档对象模型（document）

- 当一个html页面加载到浏览器的时候，那么浏览器会为每个标签都创建一个对应的对象，描述该标签的所有信息
- 我们此时所看到的网页信息实际上就是看到了这些标签的对象信息，如果我们需要操作页面的数据，我们就可以通过这些标签对象进行操作
- 图例
- ![img](https://files.catbox.moe/29phbz.png)

#### 用来获取页面节点的方法

- 获取页面的所有节点：document.all；

- nodeName:节点名字

  ```
  var    elements =document.all;
  alert(elements);
  for(var index = 0;index<elements.length;index++){
     alert("节点名："+elements[index].nodeName);
  }
  ```

  

- 通过标签属性找节点

- - document.getElementById(“标签属性id”);

  - 例

    ```
    <div id="test">
    window.onload=function(){
        var    a = document.getElementById("test");
        alert(a);
    };
    ```

    

- 通过标签名获取节点

- - document.getElementsByTagName(标签名);

  - 注：返回的是一个数组

  - 例

    ```
    <div></div>
    window.onload=function(){
         var    a = document.getElementsByName("div");
         alert(a);
    };
    ```

    

- 通过标签的Name属性获取节点

- - document.getElementByName(“标签的name属性值”);

  - 注：返回的是一个数组

  - 例

    ```
    <div name="ElName"></div>
    window.onload=function(){
        var    a = document.getElementsByName("ElName");
        alert(a);
    };
    ```

    

- 通过关系找节点

- - document可以通过一个节点，找到与它有关的节点

- - - parentNode：获取当前元素的父节点

    - 例

      ```
      window.onload=function(){
          var    a = document.getElementById("test");
          var    f = a.parentNode;
          alert(f);
          f.innerHTML="找到我了";
      };
      ```

      

- childNodes：获取当前元素的所有下一级子元素

  ```
  window.onload=function(){
  var    a = document.getElementById("test");
  var    all = a.childNodes;
  for(var    index = 0;index<all.length;index++){
      alert(all[index].nodeName);
      if(all[index].nodeType==1){
         all[index].style.background="red";
      }
   }
  };
  ```

| **类型**                         | **nodeType常数值** | **描述**                             |
| -------------------------------- | ------------------ | ------------------------------------ |
| Node.ELEMENT_NODE                | 1                  | 元素节点                             |
| Node.ATTRIBUTE_NODE              | 2                  | 属性节点                             |
| Node.TEXT_NODE                   | 3                  | 文本节点                             |
| Node.CDATA_SECTION_NODE          | 4                  | 字符数据节点（文本不会被解析器解析） |
| Node.ENTITY_REFERENCE_NODE       | 5                  | 实体引用节点                         |
| Node.ENTITY_NODE                 | 6                  | 实体节点                             |
| Node.PROCESSING_INSTRUCTION_NODE | 7                  | 处理指令节点                         |
| Node.COMMENT_NODE                | 8                  | 注释节点                             |
| Node.DOCUMENT_NODE               | 9                  | 文档节点（DOM树的根节点）            |
| Node.DOCUMENT_TYPE_NODE          | 10                 | 向为文档定义的实体提供接口           |
| Node.DOCUMENT_FRAGMENT_NODE      | 11                 | 表示邻接节点和它们的子树。           |
| Node.NOTATION_NODE               | 12                 | 代表一个符号在DTD中的声明            |

- firstChild：获取当前节点的第一个子节点

- lastChild：获取当前节点的最后一个字节点

- nextElementSibling：获取当前节点的下一个节点（兄弟节点）

- previousElementSibling：获取当前节点的上一个节点（兄弟节点）

- 创建，删除，插入节点

- - - 创建：var 节点 = document.creatElement(“标签名”);创建新元素节点
    - 节点 .setAttribute(“属性名”,”属性值”);
    - 节点.appendChild(e);将某个节点添加到该节点的最后位置
    - 节点.insertBefore(e,child);将某个新节点添加到该节点中，某个子节点之前
    - 节点.removeChild(要删除的子节点)；删除指定的直接点

- - - - 节点必须为直接父节点

- - - 例

      ```
      var    trNode = document.createElement("tr");
      var tdNode = document.createElement("td");
      trNode.appendChild(tdNode);
      ```

- 利用节点操作css

- - 我们可以通过上边获取节点的方式获取到节点，我们可以通过节点对象去操作标签的的样式
  - 语法

- - - 节点.style.要操作的样式=”值”;

#### JavaScript中常用的事件

- js有可以通过某些方式触发函数的执行，我们把这种方式称之为事件

- 点击事件（onclick()）

- - 案例

    ```
    <script>
    function    sp(elementid){
    var    a = document.getElementById(elementid);
    a.style.background="red";
    }
    </script>
    <title>无标题文档</title>
    </head>
     
    <body>
    <div    id="test" nzmd="ElName"    style="height:100px;">
                   <p    id="elp" onclick="sp('elp')">1</p>
            <a id="ela"    onclick="sp('ela')">2</a>
        </div>
    </body>
    ```

    

- 鼠标进入事件（onmouseover(),onmousemove()）

- 鼠标离开事件（onmouseout()）

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
      .box{
        width: 200px;
        height: 500px;
        display: none;
      }
      .boxOne{
        background-color: red;
      }
      .boxTwo{
        background-color: aqua;
      }
    </style>
    <script>
      function show(idName) {
        //根据id获取要显示的元素
        var el = document.getElementById(idName);
        el.style.display = "block";
      }
      function hide(idName) {
        var el = document.getElementById(idName);
        el.style.display = "none";
      }
    </script>
  </head>
  <body>
    <!--悬停事件：鼠标进入元素后触发-->
    <!--鼠标离开事件：鼠标离开元素后触发-->
    <nav>
      <a href="#" onmousemove="show('one')" onmouseout="hide('one')">导航一</a>
      <a href="#" onmousemove="show('two')" onmouseout="hide('two')">导航二</a>
    </nav>
    <div class="box boxOne" onmousemove="show('one')" onmouseout="hide('one')" id="one"></div>
    <div class="box boxTwo" onmousemove="show('two')" onmouseout="hide('two')" id="two"></div>
  </body>
</html>
```

- 获取焦点（onfocus()）

- 失去焦点（onblur()）

- - 案例

    ```
    <script>
    function    of(){
    var    a = document.getElementById("eli");
       a.value="";
    }
    function    ob(){
    var    a = document.getElementById("eli");
       a.value="有字";
    }
    </script>
    <title>无标题文档</title>
    </head>
     
    <body>
    <input    type="text" onfocus="of()" onblur="ob()"    id="eli"/>
    </body>
    <script>
    window.onload=function(){
        var    a = document.getElementById("eli");
        a.onfocus=function(){
            a.placeholder="";
       }
      a.onblur=function(){
          a.placeholder="有字";
      }
    }
    </script>
    <title>无标题文档</title>
    </head>
     
    <body>
    <input    type="text" id="eli" placeholder="hello"/>
    </body>
    ```

- 滚动事件(onscroll())

- - 案例

    ```
    <style>
                   #test{
    width:100%;
    height:100px;
    overflow:scroll;
    border:1px    solid black;
    }
        </style>
    <script>
    window.onload=function(){
    var    a = document.getElementById("test");
    a.onscroll=function(){
    a.innerHTML="aaaaaa";
    };
    };
    </script>
    <title>无标题文档</title>
    </head>
     
    <body>
    <div    id="test" >
                   啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊
        </div>
    ```

- 键盘按下并松开（onkeypress()）

- 键盘按下事件（onkeydown()）

- - onkeypress 和 onkeydown 是有区别，下面将讲解 onkeypress 与 onkeydown 事件的区别。
  - onkeypress 事件在用户按下并放开任何字母数字键时发生。但是系统按钮（例如：箭头键、功能键）无法得到识别。
  - onkeydown 事件在用户按下任何键盘键（包括系统按钮）时发生。
  - 具体区别：
  - \1. 一个放开一个没有放开，onkeydown 先于 onkeypress 发生。
  - 2.onkeypress 无法识别系统按钮。
  - 2.onkeydown 捕获的 keyCode 不区分字母大小，而 onkeypress 区分。

- 键盘抬起事件（onkeyup()）

- - 案例

    ```
    <body>
    <input type="text" id="txt">
    <script>
        document.getElementById("txt").onkeydown = function () {
            console.log("键盘按下了");
        };
        document.getElementById("txt").onkeyup = function () {
            console.log("键盘抬起了");
        };
    </script>
    </body>
    ```

    

- keyCode获取按下的键

| **数字值** | **实际键值**          |
| ---------- | --------------------- |
| 48到57     | 0到9                  |
| 65到90     | a到z（A到Z）          |
| 112到135   | F1到F12               |
| 8          | BackSpace（退格）     |
| 9          | Tab                   |
| 13         | Enter（回车）         |
| 20         | Caps_Lock（大写锁定） |
| 32         | Space（空格键）       |
| 37         | Left（左箭头）        |
| 38         | Up（上箭头）          |
| 39         | Right（右箭头）       |
| 40         | Down（下箭头）        |

- 案例

  ```
  <script>
      //页面的任何的位置.按下键盘,获取按键的值
      document.onkeydown = function (e) {
          switch (e.keyCode) {
              case 81:
                  console.log("您按下的是Q");
                  break;
              case 87:
                  console.log("您按下的是W");
                  break;
              case 69:
                  console.log("您按下的是E");
                  break;
              case 82:
                  console.log("您按下的是R");
                  break;
          }
      };
  </script>
  ```

  

- onmousedown / onmouseup 鼠标按下/抬起事件

- - 当鼠标左键或右键按下或者抬起的时候触发
  - 按下或抬起滚动轮也会触发，滑动滚动轮不能触发
  - 如果鼠标比较高级，有其他按键的情况下，按下或抬起也会触发
  - 案例

```
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div {
            width: 50px;
            height: 50px;
            background-color: pink;
        }
    </style>
</head>
<body>
<div id="dv"></div>
<script>
    document.getElementById("dv").onmousedown = function () {
        console.log("鼠标按下了");
    };
    document.getElementById("dv").onmouseup = function () {
        console.log("鼠标抬起了");
    };
</script>
</body>
```

