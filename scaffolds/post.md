---
title: {{ title }}
date: {{ date }}
author: Kiah
img: 
top: true #是否开启 TOC，可以针对某篇文章单独关闭 TOC 的功能。前提是在主题的 config.yml 中激活了 toc 选项 推荐文章（文章是否置顶），如果 top 值为 true，则会作为首页推荐文章
hide: true # 隐藏文章，如果hide值为true，则文章不会在首页显示
cover: false # true  表示该文章是否需要加入到首页轮播封面中
coverImg: #/images/1.jpg 表示该文章在首页轮播封面需要显示的图片路径，如果没有，则默认使用文章的特色图片
password: #8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92 文章阅读密码，如果要对文章设置阅读验证密码的话，就可以设置 password 的值，该值必须是用 SHA256 加密后的密码，防止被他人识破。前提是在主题的 config.yml 中激活了 
toc: false #  是否开启 TOC，可以针对某篇文章单独关闭 TOC 的功能。前提是在主题的 config.yml 中激活了 toc 选项
mathjax: false #是否开启数学公式支持 ，本文章是否开启 mathjax，且需要在主题的 _config.yml 文件中也需要开启才行
summary: #(一段话)这是你自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要
categories: 日常生活 #Markdown 文章分类，本主题的分类表示宏观上大的分类，只建议一篇文章一个分类
tags:
  - 休闲
  - 娱乐  # 文章标签，一篇文章可以多个标签

keywords: 娱乐 #Typora 文章标题,文章关键字，SEO 时需要
reprintPolicy: cc_by #文章转载规则， 可以是 cc_by, cc_by_nd, cc_by_sa, cc_by_nc, cc_by_nc_nd, cc_by_nc_sa, cc0, noreprint 或 pay 中的一个
---
