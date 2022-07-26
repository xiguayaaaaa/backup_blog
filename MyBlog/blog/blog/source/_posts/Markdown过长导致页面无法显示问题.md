---
title: Markdown过长导致页面无法显示问题
date: 2022-07-05 13:18:25
tags:
- 瞎写的
categories:
- 问题组
cover: https://img1.baidu.com/it/u=729938845,709425648&fm=253&fmt=auto&app=138&f=JPEG?w=977&h=500
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
Markdown过长导致页面无法显示问题
<!-- more -->

## 文章摘要设置

打开主题配置文件 _config.yml 文件，找到如下：

```
# Automatically Excerpt. Not recommend.
# Please use <!-- more --> in the post to control excerpt accurately.
auto_excerpt:
  enable: false
  length: 150
```

把这里的false改为true就可以了在首页启动显示文章预览了，length是显示预览的长度。

这里我们可以通过在文章使用`<!-- more -->`标志来精确控制文章的摘要预览，比如这篇文章就是在这个段落的末尾添加了该标志，所以本文在首页的预览就会显示到这个段落为止。



强烈推荐使用该`<!-- more -->`标志来控制文章的摘要预览，因为这种方式可以让摘要也按照css文件中的样式来渲染。如果使用了自动摘要的功能，你会发现文章摘要是一大团没有样式的文本，很是难看。

## 其他的文章配置

```
# ---------------------------------------------------------------
# Post Settings
# ---------------------------------------------------------------# Automatically scroll page to section which is under <!-- more --> mark.
# 自动将页面滚动到<!-- more -->标记下的地方。
scroll_to_more: false# Automatically saving scroll position on each post/page in cookies.
# 自动保存每篇文章或页面上一次滚动的地方。
save_scroll: false# Automatically excerpt description in homepage as preamble text.
# 自动在首页对文章进行摘要描述作为前言文本。
excerpt_description: true# Automatically Excerpt. Not recommend.
# Please use <!-- more --> in the post to control excerpt accurately.
# 不推荐使用自动摘要。
# 请在文章中使用<!-- more -->标志来精确控制摘要长度。
auto_excerpt:
  enable: true
  length: 200# Post meta display settings
# 文章元数据展示设置
post_meta:
  # 文本显示
  item_text: true
  # 创建时间
  created_at: true
  # 更新时间
  # 这个更新时间有点问题，因为每次重新生成文章/部署时都会刷新更新时间，不建议使用
  updated_at: false
  # 目录分类
  categories: true# Post wordcount display settings
# Dependencies: https://github.com/willin/hexo-wordcount
# 文章字数展示设置
post_wordcount:
  # 文本显示
  item_text: true
  # 文章字数统计
  wordcount: true
  # 阅读时长
  min2read: true
  # 站点总字数统计
  totalcount: true
  # 该post_wordcount的所有设置另起一行显示
  separated_meta: true
```
