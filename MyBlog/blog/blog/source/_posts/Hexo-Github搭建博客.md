---
title: Hexo+Github搭建博客
date: 2022-07-05 20:55:31
tags:
- 
categories:
- 兴趣组
cover: https://img0.baidu.com/it/u=1124800809,3510584668&fm=253&fmt=auto&app=138&f=PNG?w=1000&h=500
coverWidth: 1200
coverHeight: 490
author: xiguayaaaaa
from:
---

Hexo+Github搭建博客
<!-- more -->

搭建博客千千万，最后受欢迎的9还是Hexo和Jekyll,用户用的非常多的两个静态博客生成系统。本文就介绍利用Hexo结合github page来搭建个人博客。

## 基础知识

### 什么是Hexo？

Hexo 是一个基于 node.js 制作的快速、简洁且高效的博客框架。Hexo 可以将我们撰写的 Markdown 文档解析渲染成静态的 HTML 网页。

### Hexo和Jekyll的区别

·本地环境
Jeklly 是由 Ruby 语言编写，需要到官网下载并安装 RubyInstaller。Hexo 则需要安装 Node.js 环境。网上经常看到很多人吐槽安装 Jekyll 经常碰到各种问题。

·速度
说是比较 Hexo 和 Jeklly 这两个框架，其实要比较 Ruby 和 Node.js 的运行速度。Node.js 是一个 Javascrip t运行环境(Runtime)。实际上它是对 Google V8 引擎进行了封装。众所周知，Google JS Runtime 速度非常快，性能非常好。在本地预览上，Jekyll 是生成了页面然后进行预览，而 Hexo 是没有在根目录生成文件的，速度也快不少。因此，Hexo 在性能和速度上面更胜一筹。

·部署
Jeklly 是将整个工程源码上传到 Github 仓库，然后 Github 会自动生成静态文件。而 Hexo 需要事先在本地生成整个站点页面，再将 Html 文件、资源文件等上传到 Github 上。

·主题
Jekyll 使用 Liquid；它是有 Ruby 语言编写的开源模板语言。Hexo 使用的是 EJS；EJS 是 JavaScript 模板库，用来从 JSON 数据中生成 HTML 字符串。EJS 相对比较复杂，所以可实现的功能更加的多。从开发一个主题难度上看，Hexo 实现起来更方便、更简单些。



## 安装环境


1、本机系统：Windows 10（64位）
2、Node.js：v6.9.2LTS（64位）

## 前期准备

### 安装Node.js
简单的说 Node.js 就是运行在服务端的 JavaScript。Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。Node.js 使用了一个事件驱动、非阻塞式 I/O 的模型，使其轻量又高效。Node.js 的包管理器 npm，是全球最大的开源库生态系统。
打开官网下载链接Node.js:https://nodejs.org/en/ (选择长期服务，版本更稳定)

<img src="https://i.loli.net/2021/10/19/PWDijRHqgzxFbyn.jpg" width = "850" height = "400" div align=right />

下载完成之后直接双击安装包，只需点击下一步（默认所有选项），然后改变安装路径即可。

测试安装是否成功：

按【win+R】键，输入cmd，再按回车弹出命令窗口

输入：(显示版本行)
```
node -v 
```
```
npm -v
```
显示结果：

<img src="https://i.loli.net/2021/10/19/fDzgWhEbnkxPevL.jpg" width = "850" height = "400" div align=right />

即安装成功；

### 安装git

Git是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。 也是Linus Torvalds为了帮助管理Linux内核开发而开发的一个开放源码的版本控制软件。

<b>从一般开发者的角度来看，git有以下功能：</b>
1、从服务器上克隆完整的Git仓库（包括代码和版本信息）到单机上。
2、在自己的机器上根据不同的开发目的，创建分支，修改代码。
3、在单机上自己创建的分支上提交代码。
4、在单机上合并分支。
5、把服务器上最新版的代码fetch下来，然后跟自己的主分支合并。
6、生成补丁（patch），把补丁发送给主开发者。

打开官网下载链接：https://git-scm.com/downloads (选择windows版本即可)

<img src="https://i.loli.net/2021/10/19/7UgXJ4y3MV6Bpri.jpg" width = "850" height = "400" div align=right />


下载完成之后直接双击安装包，只需点击下一步（出下图外选项，默认所有选项），然后改变安装路径即可。

<img src="https://i.loli.net/2021/10/19/oT9CgyscVXWPnbF.jpg" width = "850" height = "400" div align=right />

测试是否安装成功：

按【win+R】键，输入cmd，再按回车弹出命令窗口，再输入：
```
git
```
显示结果:

<img src="https://i.loli.net/2021/10/19/y5LnHxaYiID93Cs.jpg" width = "850" height = "400" div align=right />


## 开始搭建

### 在Git安装目录中点击【git-bash.exe】,输入命令：（输入时引号不要删）
```
ssh-keygen -t rsa -C "Github注册的邮箱"
```
然后按四次【enter】即可，生成后如下图：

<img src="https://i.loli.net/2021/10/19/6S8LwDAmHTMvqJz.jpg" width = "850" height = "400" div align=right />

### 打开Github,点击头像-->【setting】

<img src="https://i.loli.net/2021/10/19/15flbemyaNIu4MU.jpg" width = "850" height = "400" div align=right />

### 点击【SSH and GPG keys】-->【New SSH key】

<img src="https://i.loli.net/2021/10/19/JNnuwh4dAMHFILT.jpg" width = "850" height = "400" div align=right />

### 输入title（可以随便输），但Key你需要用记事本或Notepad++打开<b>磁盘中c:/用户/用户名/.ssh/id_rsa.pub</b>然后复制粘贴里面的内容到key中，最后点击【ADD SSH key】；

<img src="https://i.loli.net/2021/10/19/uglR7p4jMUSbfxe.jpg" width = "850" height = "300" div align=right />

### 安装hexo
在想要搭建博客的目录下创建文件夹名为blog，按【win+R】键，输入cmd，再按回车弹出命令窗口，cd到创建的文件夹下，输入：
```language
npm install hexo-cli -g
```

<img src="https://i.loli.net/2021/10/19/pwBHNlgo2cdZiA4.jpg" width = "850" height = "300" div align=right />

不要关闭刚才的命令窗口，在刚才的窗口中初始化hexo，输入：

```language
hexo init 你的博客名
```

### 在博客目录中安装依赖
在刚才的窗口中
```
cd 博客名
```
```language
npm install
```
安装完成之后进行测试，窗口中输入：

```language
hexo s -p 5555
```
在浏览器上输入 localhost:5555

<img src="https://i.loli.net/2021/10/19/KFMBiULjA1yY8st.jpg" width = "850" height = "300" div align=right />

### 安装Sublime Text
打开官网下载链接：https://www.sublimetext.com/ （点击DPWNLOAD FOR WINDOWS）

<img src="https://i.loli.net/2021/10/19/kAnXiPatsr2zxDc.jpg" width = "850" height = "300" div align=right />

下载完成之后直接双击安装包，只需点击下一步（默认所有选项），然后改变安装路径即可。

打开Sublime 直接将博客目录拖进Sublime即可；

<img src="https://i.loli.net/2021/10/19/RMkyeoixVCAt81f.jpg" width = "850" height = "400" div align=right />

### hexo发布到Github
使用Sublime打开博客根目录中_config.yml 修改第16行的url 改为自己的网址（如 https://自己的博客名.github.io ）

<img src="https://i.loli.net/2021/10/20/QHMrJse8xOnjWl5.jpg" width = "850" height = "200" div align=right />

打开Github网页点击【Your repositories】 最后复制链接

<img src="https://i.loli.net/2021/10/20/u1w8kDULWQBvGzs.jpg" width = "850" height = "450" div align=right />

<img src="https://i.loli.net/2021/10/20/6cGuVNTXKWFSZsw.jpg" width = "850" height = "300" div align=right />

<img src="https://s2.loli.net/2022/07/05/YuC4zwxFHcrPOgt.jpg" width = "850" height = "350" div align=right />

在_config.yml文件最后一行添加repo
```language
repo: 
```
将你复制的链接添加到repo之后，用引号隔开（切记引号后面必须要有空格）

在最后一行添加

```language
branch: main
```
type后添加git
```language
type: git
```

如下图

![屏幕截图 2022-07-05 210636.png](https://s2.loli.net/2022/07/05/qN5nxLk7d4EfYXF.png)
在博客根目录下添加插件：

```language
npm install hexo-deployer-git --save
```

### 获取个人访问令牌

对密码身份验证的支持已于 2021 年 8 月 13 日移除。现在改用个人访问令牌。简单点说就是需要把你的密码换成 token。

在个人设置页面，找到 Settings
<img src="https://i.loli.net/2021/10/19/15flbemyaNIu4MU.jpg" width = "850" height = "400" div align=right />
找到 Developer settings
<img src="https://i.loli.net/2021/10/21/VkyOgL5Z1746mzT.jpg" width = "850" height = "350" div align=right />
选择个人访问令牌 Personal access tokens，然后点击生成令牌 Generate new token
<img src="https://i.loli.net/2021/10/21/KsVtaRpmhUSLorF.jpg" width = "850" height = "350" div align=right />
设置 token 的有效期，访问权限等，生成令牌 Generate token
<img src="https://i.loli.net/2021/10/21/6Kdwmi7Qr2MWUJf.jpg" width = "850" height = "350" div align=right />
如下为生成的令牌
<img src="https://i.loli.net/2021/10/21/LMsRWZaq8oSUwnh.jpg" width = "850" height = "350" div align=right />

<font color=RED>注意
记得把 token 保存下来，当你再次刷新网页的时候，就没办法看见了</font>


最后，把 token 直接添加远程仓库链接中，这样就可以避免同一个仓库每次提交代码都要输入 token 了。

添加到如下图位置：（使用“@”和后面内容隔开）

<img src="https://i.loli.net/2021/10/21/WCX7dgp9UNFxJ1B.jpg" width = "850" height = "200" div align=right />

### git中设置你的用户名和邮件名
 这一点很重要，因为每一个 Git 提交都会使用这些信息，它们会写入到你的每一次提交中。
 ```language
 git config --global user.name "Your Name"
 ```
 ```
 git config --global user.email "you@example.com"
 ```

### 生成提交

```
hexo g
```
```
hexo d
```
打开你的浏览器：
```language
https://博客名.github.io
```
恭喜您，您的博客现在已制作完成，现在只需要添加你喜欢的主题既可以开始你的博客之旅了。

### 添加主题

hexo主题网站：https://hexo.io/themes/
<img src="https://i.loli.net/2021/10/21/AhUeqK8sB53jp4k.jpg" width = "850" height = "400" div align=right />

找到你喜欢的主题，例如next主题 点击【next】
<img src="https://i.loli.net/2021/10/21/ciqEGsyQ3l9Oorp.jpg" width = "850" height = "400" div align=right />

按照文件中所说下载和修改即可
<img src="https://i.loli.net/2021/10/21/b16RkjZFNDQAEic.jpg" width = "850" height = "400" div align=right />

在博客根目录中打开【Git Bash Here】
```language
npm install hexo-themes-next
```
安装完成后，打开 Hexo 配置文件(_config.yml)并将theme变量设置为next.
```language
theme: next
```

### 现在来介绍常用的Hexo 命令

npm install hexo -g #安装Hexo
npm update hexo -g #升级
hexo init #初始化博客

命令简写
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo g == hexo generate #生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy #部署

hexo server #Hexo会监视文件变动并自动更新，无须重启服务器
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP
hexo clean #清除缓存，若是网页正常情况下可以忽略这条命令