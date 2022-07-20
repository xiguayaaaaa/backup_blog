---
title: Json教程
date: 2022-07-04 16:36:28
tags:
- 知识
categories:
- 知识组
cover: https://img0.baidu.com/it/u=1264698771,643931544&fm=253&fmt=auto&app=138&f=JPEG?w=640&h=404
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
Json教程
<!--more-->

## Json教程

JSON: **J**ava**S**cript **O**bject **N**otation(JavaScript 对象表示法)

JSON 是存储和交换文本信息的语法，类似 XML。

JSON 比 XML 更小、更快，更易解析。

JSON 独立于语言：JSON 使用 Javascript语法来描述数据对象，但是 JSON 仍然独立于语言和平台。JSON 解析器和 JSON 库支持许多不同的编程语言。 目前非常多的动态（PHP，JSP，.NET）编程语言都支持JSON。

```json
{
    "sites": [
    { "name":"百度" , "url":"www.baidu.com" }, 
    { "name":"google" , "url":"www.google.com" }, 
    { "name":"微博" , "url":"www.weibo.com" }
    ]
}
```

### Json语法规则

JSON 语法是 JavaScript 对象表示语法的子集。

- 数据在名称/值对中
- 数据由逗号分隔
- 大括号 **{}** 保存对象
- 中括号 **[]** 保存数组，数组可以包含多个对象

### JSON 名称/值对

JSON 数据的书写格式是："key":"value"

### JSON 值数据类型

JSON 值可以是：

- 数字（整数或浮点数）:JSON 数字可以是整型或者浮点型，例如，"age":18
- 字符串（在双引号中）:例如，"name":"王钢蛋"
- 逻辑值（true 或 false）:JSON 布尔值可以是 true 或者 false，例如，"flag":true
- 数组（在中括号中）:JSON 数组在中括号 **[]** 中书写，JSON 中数组值必须是合法的 JSON 数据类型（字符串, 数字, 对象, 数组, 布尔值或 null）。数组可包含多个对象。
- 对象（在大括号中）:JSON 对象在大括号 **{}** 中书写，例如，{"data":{"name":"张三","age":18}}
- 对象可以包含多个 **key/value（键/值）**对。key 必须是字符串，value 可以是合法的 JSON 数据类型（字符串, 数字, 对象, 数组, 布尔值或 null）。key 和 value 中使用冒号(:)分割。每个 key/value 对使用逗号(,)分割。
- null：例如，“name”:null

### JSON访问

#### 访问JSON对象

```javascript
let str = '{"name":"张三","age":18}'
//将JSON格式的字符串转换成JSON对象
let obj = JSON.parse(str)
console.log(obj.name)
console.log(obj.age)
```

#### 访问JSON数组

```javascript
let ary = '["google","baidu","sohu","sina"]'
let obj = JSON.parse(ary);
		
console.log(obj[0]);
console.log(obj[1]);
```

#### 复杂情形

```javascript
let str = '{"students":[{"name":"张三","age":18},{"name":"李四","age":18}]}'
let obj = JSON.parse(str);
		
let ary = obj.students;
for(let i = 0;i<ary.length;i++){
	console.log(ary[i].name+"============"+ary[i].age);
}
```

### JSON.parse()

JSON 通常用于与服务端交换数据。

在接收服务器数据时一般是字符串。

我们可以使用 JSON.parse() 方法将数据转换为 JavaScript 对象。



