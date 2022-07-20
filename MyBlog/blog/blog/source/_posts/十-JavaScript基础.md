---
title: (十)JavaScript基础
date: 2022-07-08 20:25:49
tags:
- 知识
categories:
- 前端组
cover: https://tse4-mm.cn.bing.net/th/id/OIP-C.lNqh_BOnndzbRVu0hCOSIgHaCm?pid=ImgDet&rs=1
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
(十)JavaScript基础
<!--more-->

## 10.1 概述

JavaScript是一种属于网络的脚本语言,已经被广泛用于Web应用开发,常用来为网页添加各式各样的动态功能,为用户提供更流畅美观的浏览效果。通常JavaScript脚本是通过嵌入在HTML中来实现自身的功能的。

- 是一种解释性脚本语言（代码不进行预编译）。
- 主要用来向HTML（标准通用标记语言下的一个应用）页面添加交互行为。
- 可以直接嵌入HTML页面，但写成单独的js文件有利于结构和行为的分离。
- 跨平台特性，在绝大多数浏览器的支持下，可以在多种平台下运行（如Windows、Linux、Mac、Android、iOS等）。

Javascript脚本语言同其他语言一样，有它自身的基本数据类型，表达式和算术运算符及程序的基本程序框架。Javascript提供了四种基本的数据类型和两种特殊数据类型用来处理数据和文字。而变量提供存放信息的地方，表达式则可以完成较复杂的信息处理。

## 10.2 JavaScript能做什么

- 使网页具有交互性，例如响应用户点击，给用户提供更好的体验
- 可以处理表单，检验用户的输入，并提供及时反馈节省用户时间。例如，表单中要你输入电子邮箱而你却输入一个手机号，那么应该给你一个提醒。
- 还可以根据用户的操作，动态的创建页面。例如，发邮件时，添加附件操作。
- 设置cookie，cookie是存储在浏览器上的一些临时信息，例如你浏览过的网站地址，使用过的用户名
- JavaScript 是有规律地重复的HTML元素简化，减少下载时间。
- 浏览器与服务器进行数据通讯，比如现在最流行的Ajax异步传输；

## 10.3 JavaScript构成

- JavaScript由以下三部分组成：

- - ECMAScript，它用来描述语法和基本对象
  - 文档对象模型Doucment Object       Model（DOM），用来处理网页内容

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630651195487-efff79bc-a3b0-45b8-9a7a-faf1c6d7abda.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 浏览器对象模型Borwser Object Model（BOM），用来处理浏览器交互

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630651202360-0b177732-6264-4def-9a1b-fdda98bbc257.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

## 10.4 JavaScript的开发环境与运行环境

- JavaScript为轻型脚本语言，可在任意文本编辑器中编辑
- 由于JavaScript是内嵌在HTML中执行，所以其运行环境即浏览器

## 10.5 JavaScript的使用

- JavaScript需在HTML中内嵌运行，其内嵌方式有两种：

- - 在网页中创建\<script>\</script>,在标签之间写JavaScript代码

```javascript
<script>
  	alert("hello world")
<script>
```

- - 在外部创建“.js”文件，通过\<script src="文件路径">引入到HTML文件中执行

```html
<head>
	<script src="xxx/xxx.js"></script>
</head>
```

## 10.6 JavaScript基础

- 值

- - 数字类型的值（数字）
  - 算术值（加减乘除等运算，需要两个或两个以上的数字）
  - 特殊数字

- - - 在JavaScript中有三个特殊数值，他们被视为数字，但其行为不像普通数字那样
    - Infinity和-Infinity表示正无穷大和负无穷大
    - NaN代表不是数字，就是不当的算数运算得到不当的值（比如：0/0或者Infinity-Infinity都会得到这样的值）

- - 字符串（用于表示文本，使用引号引起来即可）

- - - 在字符串中还需要注意

- - - - 在引号中添加特殊字符时比较难加，但是只需要添加反引号”`“就可解决这个问题

console.log(`hello my   "son"`);

- 转义符（\）

- - 出现在引用文本中，表示后面有特殊字符
  - 换行符（\n）
  - 制表符（\t）
  - 如果希望字符串中的斜杠只是斜杠，可以使用两个斜杠

console.log("l   input \"\\n\"");

- 运算符

- - 一元运算符

- - - 在JavaScript中并非所有的运算符都是由符号构成的，还有由单词构成的符号，如：typeof运算符用来生成一个字符串，表示你输入数据的类型

console.log(typeof   2.2);console.log(typeof   "hello");

- 布尔值

- - 比较运算符（>,<,<=,<=……）

- - - 比较运算符属于二元运算符

console.log(1<2)

- 字符串也是可以比较的

| console.log(a>b)                                             |
| ------------------------------------------------------------ |
| 字符串在比较时大致时按照字母的顺序比较，而小写字母的大于大写字母，在字符串比较是JavaScript从左道右遍历字符按照字母的unicode编码进行比较 |
| 注意：在JavaScript中只有一个值不等于它自己，他就是NaN（不是数字）console.log(NaN==NaN)返回false |

- 逻辑运算符（与，或，非）

- - &&:表示逻辑与，表示结果为真才为真

| console.log(true&&false) | false |
| ------------------------ | ----- |
| console.log(true&&true)  | true  |
|                          |       |

- - ||：表示逻辑或，表示一个为真，则为真

| console.log(true\|\|false)  | true  |
| --------------------------- | ----- |
| console.log(false\|\|false) | false |

- - !：表示逻辑非，表示取反
  - 在上边两种运算符混合使用时需要注意他们的优先级，一般情况下是,||具有最低优先级，然后时&&，然后是比较运算符，再然后时其他运算符
  - 三元运算符，由问号和冒号写成

| console.log(true?1:2)  |
| ---------------------- |
| console.log(false?1:2) |

- 空值

- - 再JavaScript中使用null和undefined表示空值

- 自动类型转换

- - JavaScript的包容性时相当高的，几乎可以接受你给他的任何程序
  - 当运算符应用不同类型的值时，JavaScript会使用一组规则自动将值转换成所需要的类型供你使用（强制类型转换）

| console.log(8*null)-->0             |
| ----------------------------------- |
| console.log("3"-1)-->2              |
| console.log("3"+1)-->31             |
| console.log("six"*1)-->NaN          |
| console.log(false==0)-->true        |
| console.log(null==undefined)-->true |
| console.log(null==0)-->false        |

- 表达式

- - 生成值得代码片段称之为表达式

console.log(1+1);

- 绑定（变量）

- - ·JavaScript为了让程序中得数据保持提供了一个称为绑定（binding）或变量（variable）得东西

- - - let属于JavaScript关键字表示将定义一个绑定，它得后面是绑定名称，如果我们想给它一个值，则由"="运算符和表达式来完成

| let a =   1*2                         |
| ------------------------------------- |
| let num =   10; console.log(num*num); |

- - - 当绑定值指向一个值时并部意味着它永远时该值，"="运算符随时可以更新绑定赋予绑定新值

let   name="张三";conlose.log(name);name   = "李四";console.log(name);

- - - 在JavaScript中不单单可以使用let去做绑定,var和const两个也可以用于绑定

| var   name="hello";console.log(name);                        |
| ------------------------------------------------------------ |
| const demo   = "world";console.log(demo);                    |
| console.log(name+demo);                                      |
| 注：1.var全称(variable)表示变量，多用于以前得JavaScript中声明绑定2.const全称（constant），表示定义一个常量绑定，只要它存在，它就一直指向相同得值 |

- JavaScript语句

- - JavaScript语句是发给浏览器的命令
  - 这些命令的作用是告诉浏览器要做的事情
  - 比如

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630652275534-6e34e0ea-ce7f-4cb2-b9f5-a303441fbb5b.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ |
| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630652282839-d8f3b6f0-bb99-4311-af61-9ec9d1d592a7.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| 解析：点击hello world后，触发JavaScript点击事件（onclick点击事件，点击后innerHTML替换标签里的内容，即把”hello world“替换成“世界 你好”） |

- 分号

- - 分号用于分隔JavaScript语句
  - 通常我们在每条可执行的语句结尾添加分号，代表作一句JavaScript语句的结束
  - 使用分号的另一个好处就是。。。。能在一行多写点代码嘛

- JavaScript代码

- - JavaScript代码是JavaScript语句的序列
  - 浏览器按照编写顺序依次执行每条语句

- JavaScript代码块

- - JavaScript可以分批地组合起来
  - 代码块以左花括号开始，以右花括号结束
  - 代码块的作用是一并执行语句序列

- 示例

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630652313702-584a551d-bd15-4e8c-873f-304b09194343.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ |
| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630652326450-8100dccd-e3b6-4e7d-afbc-1246a23c2fc5.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

- JavaScript语句标识符

- - JavaScript语句通常以一个语句标识符为开始，并执行该语句。
  - 语句标识符是保留关键字不能作为变量名使用
  - JavaScript语句标识符（关键字）

| 语句       | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| break      | 用于跳出循环                                                 |
| catch      | 语句块，在try语句块执行出错时执行catch语句块                 |
| continue   | 跳过循环的一个迭代                                           |
| do...while | 执行一个语句块，在条件语句为true时继续执行该语句块           |
| for        | 在条件语句为true时，可以将代码块执行指定的次数               |
| for...in   | 用于遍历数组或对象的属性（对数组或者对象的属性进行循环操作） |
| function   | 定义一个函数                                                 |
| if...else  | 用于基于不同的条件来执行不同的动作                           |
| return     | 退出函数                                                     |
| switch     | 用于基于不同条件来执行不同的动作                             |
| throw      | 抛出错误                                                     |
| try        | 实现错误处理，与catch一同使用                                |
| var        | 声明一个变量                                                 |
| while      | 当条件语句为true时，执行语句块                               |

- 代码折行

| document.write("hello   \ world")； | 但是不能这么折行document.write\("hello world")； |
| ----------------------------------- | ------------------------------------------------ |
|                                     |                                                  |

## 10.7 JavaScript数据类型

- javascript属于弱语言，它的变量没有明确的数据类型，它的数据类型是由它存储的值自己推断出来的
- 常见数据类型

| **数据类型** | **具体描述**                   |
| ------------ | ------------------------------ |
| number       | 能存储整数和小数类型           |
| string       | 用单引号或双引号来声明的字符串 |
| boolean      | 只能是两个值选择：true、false  |
| undefined    | 变量被声明后，但未被赋值       |
| object       | javascript中的对象、数组和null |

- 在JavaScript中可以使用typeof()函数来检查变量的返回值类型

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630655653508-92e34507-ef26-46c0-92e5-fd7054983ad7.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- JavaScript拥有动态类型，这意味着相同的变量可用作不同的类型

var x；//x为undefinedvar   x = 5；//x为数字var   x = "hello";//x为字符串

- JavaScript字符串

- - 字符串是存储字符的变量
  - 字符串可以是引号中的任意文本。可以使用单引号或者双引号

var name =   "tom";var name =   'tom';

- 也可以在字符串中使用引号，只要不匹配包围字符串的引号即可

var answer   = "let'go";var answer   = "my name is 'tom' ";

- JavaScript数字

- - JavaScript只有一种数字类型。数字可以带小数点。

var a = 3;var b =   3.14;

- 极大或极小的数字可以通过科学计数来书写

| var a =   123e5;//12300000 |
| -------------------------- |
| var b =   123e-5;//0.00123 |

- JavaScript布尔

- - 布尔（逻辑）只能有两个值：true或false

var a =   false;var b =   true;

- 布尔常用在条件测试中。这个我们将在之后详解
- JavaScript数组

- - 详见10.8节

- JavaScript对象

- - 详见10.9节
  - 对象由花括号分隔。在扩号内部，对象的属性以名称和值对的形式（键值对 name：value）来定义，属性由逗号分隔
  - 对象有两种寻址方式：

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630655910721-0a48b0a7-993c-45ca-a851-9d8a9f0216b6.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_17%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630655916757-28032444-e669-4911-8a08-0adc9bd721a0.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_11%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

- Undefined和Null

- - Undefined表示变量不含值
  - Null可以通过将变量的值设置为Null来清空变量

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630655925751-c01fd5d4-f3f1-4a93-b80f-4aff98f02075.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630655944042-42c54dea-cfb9-4ae5-b05b-700a4977857f.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

- 声明变量类型

- - 当声明新变量时，可以使用关键词“new”来声明其类型

var   name = new String; var age   = new Number;var   money = new boolean;var   cars = new Arrays;var   person = new Object;

## 10.8 数组

- 什么是数组

- - 数组对象是使用单独的变量名来存储一系列相同类型的值
  - 数字可以用一个变量名存储所有的值，并且可以用变量名访问任何一个值
  - 数组中的每个元素都有自己的ID，以便它可以很容易地被访问到

- 创建数组，有几种不同的方式

- - 常规方式

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656318089-149f266a-0657-417b-8911-de077af3a0f9.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 简洁方式

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656324807-3401185c-a1b8-4ed5-beb7-cf10312d944f.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 字面方式

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656333229-64159517-3a00-411f-9c39-8fd82965fabd.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 访问数组

- - 通过上边的几个例子，大家应该能看出来数组是怎么访问的
  - 语法：数组名[下标] 

arr[1]

- - 在数组中[0]代表数组的第一个元素，[1]则代表的是第二个元素

- 来个数组式循环弹窗看看

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656416554-a1696c63-5193-447f-8671-1517574a0e6b.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_38%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

弹窗完事了，再顺道在页面中把数组里的值打印出来看看![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656471840-ecbb7e13-667b-4345-97a4-60a849ed451e.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_37%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 在一个数组中可以有不同的对象

- - 所有的JavaScript变量都是对象，数组元素是对象，函数也是对象
  - 因此，我们可以在数组中有不同的变量类型
  - 我们可以在一个数组中包含对象元素，函数，数组

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656507497-a9128903-1f51-48a0-af1b-f9071ff0f389.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 数组方法和属性

- - 使用数组对象预定义属性和方法

| var    a = 数组名.length    //length元素的数量               |
| ------------------------------------------------------------ |
| var    b = 数组名.indexOf("需要索引的字段")  //括号里面为索引值 |

- 更多的实例

- - 合并两个数组-concat()

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656639810-73054345-0af6-4c4c-9ba2-fc7620a200bc.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_14%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656647809-524de2d0-01a1-475f-8190-1ae2329987a5.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

- - 合并三个数组-concat()

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656677924-8ac387d8-aeda-4de2-bb7f-a6e719d44605.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656681979-9220fb0b-ae48-4483-b788-aa30761ed63e.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

- 用数组的元素组合字符串-join()

- - join()方法用于把数组中的所有元素放入一个字符串
  - 元素是同过指定的分隔符分隔的

| arrayObject.join(separator)                                  |
| ------------------------------------------------------------ |
| separator：指定要使用的分隔符，如果省略改参数，则使用逗号作为分隔符 |

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656712682-e75f5712-761e-4ad0-9d2e-e3d46917c3ac.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_19%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ |
| 点击前![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656792868-b57e6395-7e1b-4fe0-bfbf-3097f9045020.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)点击后![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656804077-1e9c4969-4c6a-4c0c-95b2-aece511e9d18.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_11%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656829884-022208bc-cf0a-4e17-bc1d-9e3fe8f751f4.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_22%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ |
| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656840313-375d5f2a-6526-4cdd-b076-4817ed5fabc0.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

- 删除数组的最后一个元素-pop()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656953405-b87be9c8-c90c-445e-8960-44bf3532e01d.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 数组的末尾添加新的元素-push()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656962674-6cef5d2d-3acd-464b-b246-c412e5b99bc7.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 将一个数组中的元素的顺序反转排序-reverse()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656973478-9c465b63-bed9-4d93-845c-492bcf418b71.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_22%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 删除数组的第一个元素-shift()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630656988336-96687b65-74b8-49a1-8576-75594e429520.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 从一个数组中选择元素-slice()

- - slice()方法可提取字符串的某个部分，并以新的字符串返回被提取的部分
  - 语法

stringObject.slice(start,end)

- - 返回值

- - - 一个新的字符串，包括字符串stratObject从strat开始（包括strat）到end结束（不包括end）为止的所有字符串

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657004800-d8713e65-4d1b-4835-8958-baf47b76d95a.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 数组排序（按字母顺序升序）-sort()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657014582-bdb1c470-3355-4e67-ad14-52c659845403.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 数字排序（按数字顺序升序）-sort()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657037116-d77644e4-9970-43ba-8247-14f9811d9daf.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 数字排序（按数字顺序降序）-sort()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657065901-7faa18d1-af03-443f-b5d2-d4c12611b404.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 在数组的第二位置添加一个元素 -splice()

- - - splice()方法用于插入，删除，或者替换数组的元素
    - 语法

arrayObject.splice(index,howmant,element1....,element1)

| 参数     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| index    | 必需。规定从何处添加/删除元素。该参数是开始插入和(或)删除的数组元素的下标，必需是数字哦 |
| howmant  | 必需。规定应该删除多少元素。必须是数字，但可以是（0）。如果未规定此参数，则删除从index开始到原数组结尾的所有元素 |
| element1 | 可选。规定要添加到数组的新元素。从index所指的下标处开始插入  |
| elementN | 可选。可向数组添加若干元素。                                 |

- - 返回值

- - - 如果从arrayObject中删除了元素，则返回的是含有被删除的元素的数组

- 注意：splice()方法和slice()方法的作用是不同的，splice()方法会直接对数组,行修改。
- 下边的这个例子就是替换了下标“1”至“3”里面的内容，包含1和3下标的内容，也就是说我把数组里的“33，22，66”替换成了“88,44”。

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657083608-3d4f358b-4c67-4628-b6f0-13a495c3ecd9.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_20%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 转换数组到字符串 -toString()

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657093306-a84ce473-7c65-478f-b512-a6d76c5929ff.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_18%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- 在数组的开头添加新元素 -unshift()

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657101064-7db40d88-68aa-4bed-98ba-96f27ed56b9b.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_17%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657111628-83befa05-ad97-4553-952f-75f9d40b5144.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_13%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

## 10.9 对象

- JavaScript对象

- - 在JavaScript中，对象是拥有属性和方法的数据。

- - - 属性是与对象相关的值
    - 方法是能够在对象上执行的动作

- - 对象也是一个变量，但对象可以包含多个值（多个变量）

![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657330235-d51b4bdc-70d3-4b9b-977b-a66c32d33174.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_16%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10)

- - 上边这个例子中，三个值（**"Lamborghini",999999,"black"**）赋予变量car
  - 三个变量（"neme",price,color）赋予变量car
  - JavaScript对象是变量的容器
  - 定义JavaScript对象是可以跨越多行，空格跟换行不是必须的

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657337152-f7388e63-dcdc-4916-929a-f6f523d3b3a7.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_41%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ |
| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657359063-4ae2da29-2812-4f6d-9e8f-0f85361ab3d6.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_12%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |

- 对象属性

- - JavaScript对象是变量的容器
  - JavaScript对象是键值对的容器
  - 键值对的基本写法为name:value（上边的例子就是喽）
  - 键值对在JavaScript对象中统称为对象属性。
  - 访问对象属性

- - - 可以用对象名点属性（如：person.one）
    - 也可以用对象名["属性"]（如：person["one"]）

| ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657371647-620ad6cf-4996-4ec9-b676-c8aadde3a394.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_17%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) | ![img](https://cdn.nlark.com/yuque/0/2021/png/22038106/1630657376463-7a710ad9-a526-457b-a68d-f3972c9f4bc4.png?x-oss-process=image%2Fwatermark%2Ctype_d3F5LW1pY3JvaGVp%2Csize_11%2Ctext_Qnl0ZeWtpumZog%3D%3D%2Ccolor_FFFFFF%2Cshadow_50%2Ct_80%2Cg_se%2Cx_10%2Cy_10) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

- 对象方法

- - 对象的方法定义了一个函数，并作为对象的属性存储
  - 对象方法通过添加()调用（当成函数调用）
  - 下边的这个例子访问了person对象的all()方法（如果直接访问person对象的all属性，它将作为定义一个函数的字符串返回，也就是说把后边的代码直接返回，并且打印出来）

- - - 访问方法（例：person.all()）
    - 访问属性（例：person.all）