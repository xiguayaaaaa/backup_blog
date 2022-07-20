---
title: Java基础
date: 2022-07-15 18:52:12
tags:
- Java
categories:
- 后端组
cover: https://www.itprotoday.com/sites/itprotoday.com/files/styles/article_featured_retina/public/java-logo.png?itok=Ch4V9Is3
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from: 
---
Java基础
<!--more-->

# 一.Java概述

### Java跨平台实现

1. Java源代码在编写过后，会编译成平台无关的字节码文件，该文件不依赖于任何平台
2. Java针对不同的平台开发了不同的JVM，当程序运行时由JVM将字节码文件转换成对应平台的指令

### Java的特点

1. 简单性
2. 跨平台
3. 分布式
4. 面向对象
5. 安全性
6. 多线程

### Java源代码中注意事项

1. Java源文件的命名和类名一致，并且首字符大写，如果有多个单词，所有单词的首字母均大写。
2. main()写法固定，public static void main(String[] args);
3. System中首字母大写

### 技术名词

JDK(Java Develop Kit):Java 开发工具

JRE(Java Runtime Environment)：Java 运行环境

JVM(Java Virtual machine )：Java虚拟机

# 二.Java标识符和运算符

Java是一门强类型语言，所谓的强类型语言，可以理解为包含以下2层含义：

1. 所有的变量都必须先声明，后使用
2. 变量的类型一旦确定，那么变量的值必须和数据类型相匹配

## Java标识符

标识符：类名、方法名、变量名统称为标识符

1. 可以包含数字、字母、下划线，$，不能以数字开头
2. 不能包含除了_，$以外的特殊字符。
3. 不能使用Java关键字

| abstract | continue | for        | new       | switch       |
| -------- | -------- | ---------- | --------- | ------------ |
| assert   | default  | if         | package   | synchronized |
| boolean  | do       | goto       | private   | this         |
| break    | double   | implements | protected | throws       |
| byte     | else     | import     | public    | throw        |
| case     | enum     | instanceof | return    | transient    |
| catch    | extends  | int        | short     | try          |
| char     | final    | interface  | static    | void         |
| class    | finally  | long       | strictfp  | volatile     |
| const    | float    | native     | super     | while        |

**示例**

```java
/**
 * 标识符的命名规范
 * 1.
 * 2.不能包含除了$,_以外的字符
 * 3.不能包含关键字
 * @author MR.W
 */
public class Identifier {
	//错误原因：不能以数字开头
//	int 1ab;
	int _abc;
	int abc_;
	int a_bc;
	int abc1;
	int $abd;
	int ab$d;
	int abd$;
	//错误原因，包含除了$，_以外的特殊符号
//	int abc-;
//	错误原因，使用了Java关键字
//	int instanceof;
	public void abc() {
	}
}
```

## Java命名方式

1. 帕斯卡命名法：所有单词首字母均大写。适用于类名，例如：StudentManager
2. 驼峰命名法：第一个单词的首字母小写，如果有多个但是，其余单词首字母均大写，适用于方法名，变量名。例如：studentAge，studentGender

## Java数据类型

1. 基本类型：byte short int long float double boolean char
2. 引用类型: 数组， 类，接口

## 变量的声明和初始化

```
数据类型  变量名 [=值];
```

## Java数据类型

| 整型  | 字节长度 | 取值范围                                             |
| ----- | -------- | ---------------------------------------------------- |
| byte  | 1        | -128~127                                             |
| short | 2        | -32768~32767                                         |
| int   | 4        | -2 147 483 648~2 147 483 647                         |
| long  | 8        | -9 223 372 036 854 775 808~9 223 372 036 854 775 807 |

| 浮点型 | 字节长度 | 取值范围                                         |
| ------ | -------- | ------------------------------------------------ |
| float  | 4        | ±3.402 823 47E+38F（有效位数为6-7位）            |
| double | 8        | ±1.797 693 134 862 315 70E+308（有效位数为15位） |

| 布尔型  | 取值范围   |
| ------- | ---------- |
| boolean | true/false |

| 字符型 | 取值范围 |
| ------ | -------- |
| char   | 0-65535  |

## 数据类型转换

1. 低类型-->高类型：自动转
2. 高类型-->低类型：强制转换

```
int a = 10;
byte b = (byte) a;
```

## 运算符

### 运算符类型

1. 算数运算符

2. 赋值运算符

3. 位运算符

4. 比较运算符

5. 逻辑运算符

### 运算符优先级

| 运算符说明         | Java运算符                              |
| ------------------ | --------------------------------------- |
| 分隔符             | , [] () {} . ;                          |
| 单目运算符         | ++ --  ~  ！                            |
| 强制类型转换运算符 | (type)                                  |
| 乘法/除法/求余     | */ %                                    |
| 加法/减法          | +-                                      |
| 移位运算符         | << >> >>>                               |
| 关系运算           | < <= >= > instanceof                    |
| 等价运算符         | == !=                                   |
| 按位与             | &                                       |
| 按位异或           | ^                                       |
| 按位或             | \|                                      |
| 条件与             | &&                                      |
| 条件或             | \|\|                                    |
| 三目运算符         | ?:                                      |
| 赋值               | = += -= *= /= &= \|= ^= %= <<= >>= >>>= |

# 三.流程控制

1. 顺序结构：通常而言，我们的代码，根据书写的顺序在上而下执行。
2. 分支结构：对多种可能出现的情况进行判断：单分支，双分支，多分支
3. 循环结构：同一段代码片段多次执行

## 顺序结构



## 分支结构

### if 单分支

```java
if(逻辑表达式){
    //代码
}
```

### if 双分支

```
if(逻辑表达式){
	//逻辑表达式结果为true，执行此处的代码
}else{
	//逻辑表达式不成立，则执行此处的代码
}
```

### if多分支

```
if(逻辑表达式){

}else if(逻辑表达式){

}else if(逻辑表达式){

}else{

}
```

1. 请将101转换成二进制，并将二进制的前3位替换为1，并求出原码
2. 请输入一个年份，并判断是否是闰年
3. 请输入一个数，判断是否是质数



























































































































https://www.yuque.com/docs/share/8290264f-2175-46ce-8b20-711eac7ac369?# 《第1章 Java语言概述》密码：syl5

https://www.yuque.com/docs/share/b9feb7da-7c3c-4ccb-8542-52a34ad5d965?# 《第2章 Java数据类型和运算符》密码：ekp0

https://www.yuque.com/docs/share/89bb9cac-ccd1-44dd-b2e2-e11933c44c39?# 《第3章 流程控制》密码：zk84

https://www.yuque.com/docs/share/5b051183-1e6a-4c80-904f-17070f1c9653?# 《第4章 数组》密码：mg6w