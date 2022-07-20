---
title: SpringBoot笔记(一）
date: 2022-07-07 17:28:39
tags:
- 知识
categories:
- SpringBoot
cover: https://pic2.zhimg.com/v2-704d04346a5e35b9bd3a4923732a589d_180x120.jpg
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
SpringBoot笔记(一）
<!--more-->
处理静态资源
***
在springboot中，可以使用以下方式处理静态资源：
+ webjars：localhost:8080/webjars/...
 百度输入webjars官网，可以找到很多资源的maven依赖方式，如jQuery，bootstrap等等。
+ public，static，/**，resource：localhost:8080/
其中优先级：resource>static(默认)>public。

首页订制
***
+ 我们一般通过controller跳转到index首页，将index.html放入templates包中，
  需导入模板引擎thymeleaf依赖。

模板引擎thymeleaf
***
+ 我们要使用thymeleaf，需要在html文件中导入命名空间的
  约束`<html lang="en" xmlns:th="http://www.thymeleaf.org">`，方便提示。
  

thymeleaf在html标签中输入th无提示的问题解决
***
+ 听说IDEA默认的thymeleaf版本是2.X版本，2.X版本有不少的功能缺陷，
但是据说现在IDEA提高了默认的thymeleaf版本，导入前文的依赖后3.X版本
的会一同下载下来，并没有去考证，死马当做活马医，手动升级了版本，
在pom.xml文件的 properties 标签中添加以下代码：
`<properties>
         <thymeleaf.version>3.0.11.RELEASE</thymeleaf.version>
         <thymeleaf-layout-dialect.version>2.1.1</thymeleaf-layout-dialect.version>
 </properties>`
 [原文连接](https://blog.csdn.net/qq_43446147/article/details/108000547)

前端页面模板下载
+ [连接](https://www.php.cn/) "首页->资源下载"

首页配置
+ 所有页面的静态资源都需要使用thymeleaf接管,@{}.

页面国际化
+ (国际化:internationalization) i与n之间有18个字母,故称i18n,
在resource下创建i18n文件夹.
+ 三个文件:默认/英文/中文 可以一个页面实现多个语言编码
+ 在application.properties中添加`spring.messages.basename=i18n.文件名`
+ 国际化页面前端页面用#{}取值.
+ 切换中文/English config中创建类实现接口LocaleResolver,配置解析请求.
+ 步骤: 
    * 我们需要配置i18n文件
    * 我们如果需要在项目中进行按钮自动切换,我们需要自定义一个组件LocaleResolver
    * 记得将自己写的组件配置到spring容器@Bean

登录＋拦截器
+ 拦截未登录直接通过地址访问管理员页面

定义Data的输入格式
+ 如果不做如何处理,日期格式输入格式为`	Wed Apr 27 22:58:12 CST 2022`
+ 我们可以使用dates.format来定义日期的输出格式，如
    `#dates.format(emp.getBirth(),'yyyy-mm-dd')` 
    yyyy-mm-dd hh-mm-ss表示年-月-日 时-分-秒
+ 也可在application.properties中加入`spring.jackson.date-format=yyyy-mm-dd`

