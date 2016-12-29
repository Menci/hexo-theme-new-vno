hexo-new-vno
========

这个主题是原创为 [onevat 的 vno](https://github.com/onevcat/vno)，它遵从简洁和响应式的设计风格，拥有一个独立的封面，易于集成的 Disqus 评论和多说系统，Google Analytics，字体图标以及多种颜色。
此主题的 Hexo 版本由[空谷幽兰](http://mlongbo.com/)最先创建，但是已不维护。
我加了一些功能及对 Bug 的修复，所以重新创建一个，[GitHub 地址](https://github.com/monniya/hexo-theme-new-vno.git)。

## Demo Show

[Demo: 我的博客](http://monniya.com)

![主页封面](source/images/show/home.png)

![文章列表](source/images/show/list.jpeg)

## 封面

### 图片和颜色

将您的封面图片放到主题的 `source/images/` 下，将图片文件改名为 `background-cover.jpg` 或修改` _config.yml` 中 `background` 的 `cover` 字段值即可。您也可以改变封面的颜色。找到 `_config.iml` 中` background` 的 `color` 字段值，然后替换成您需要的颜色即可。默认为您提供了七种选择：

* `cover-blue` - #2568A3
* `cover-green` - #156F78
* `cover-purple` - #493252
* `cover-red` - #E25440
* `cover-orange` - #FB9C50
* `cover-slate` - #3D4260
* `cover-disabled` - 透明

### 头像和简介

头像可以在封面中显示，将头像文件放到全局的 `source/images/` 下，修改 `_config.yml` 中的 `logo` 字段值即可。

您还可以在封面页上写一个简短的介绍，填写全局的 `_config.yml`（注意：不是主题下的 `_config.yml`）中的 `description` 字段值，支持 HTML 标签。


## Installation

### Install 安装

``` bash  
$ git clone https://github.com/monniya/hexo-theme-new-vno.git themes/new-vno
```

### Enable 主题启用设置

设置全局的 `_config.yml`

```
theme: new-vno
```


## Configuration 主题设置
设置主题目录下的 `_config.yml`

```yml
# menu 子菜单，可自定义
menu:
  # Archives: /archives
  黄金屋: /favourite
  时光机: /favourite/time.html
  # 我是: /aboutme
# rss 需安装插件 hexo-generator-feed，详细请看：http://monniya.com/2016/02/24/create-rss/
rss: /atom.xml
# description 配置内容会出现在 meta 标签中，因此会被搜索引擎抓取
description: 

# 不填写的链接则不显示
social:
  weibo: http://weibo.com/monniya
  github: https://github.com/monniya
  stack_overflow: 
  facebook: 
  twitter: 
  google_plus: 
  qq: # 填写链接

page_comment: true

# 封面中的头像
logo: /images/avatar.jpg
background:
  cover: /images/background-cover.jpg
  color: cover-purple

archive_date_format: MMM DD
fancybox: true
search: false # 是否启用搜索

# 多说的帐号名，不配置则不启用，使用 disqus 请去全局 _config.yml 中配置 disqus_shortname
duoshuo_shortname: 
comment_on_non_post: false # 在非 post、page 的页面（如首页）内评论

google_analytics: 谷歌跟踪ID
baidu_tongji: 百度统计识别码
favicon: /images/avatar-small.png
```
谷歌跟踪 ID：
![谷歌统计](source/images/show/google-analytics.jpeg)
百度统计识别码：
![百度统计](source/images/show/baidu_tongji.jpeg)

### 文章

喵神没有设置 `categories`，只用 `tags`
例如：
```yml
---
title: 文章名称
date: 2016-03-03 10:46:46
tags: 分类
---
```
![文章](source/images/show/article.jpeg)

### 搜索
本主题移植了由 [PPOffice](https://ppoffice.github.io/) 开发的 [icarus](https://github.com/ppoffice/hexo-theme-icarus) 主题中的站内搜索（insight search），使用时需要安装 `hexo-generator-json-content` 生成索引。

```
npm install hexo-generator-json-content --save
```

将主题目录下 `_config.yml` 中的 `search` 字段修改为 `true` 即可使用。