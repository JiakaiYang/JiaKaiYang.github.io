---
title: 拥有自己的图床PicGo
author: Kiah
top: true
hide: false
cover: false
toc: true
mathjax: false
categories: 软件(知识)分享
tags:
  - picgo
  - 图床
keywords: 把图片放到网上(图床)
reprintPolicy: cc_by
date: 2022-02-14 17:13:15
img: https://cdn.jsdelivr.net/gh/JiakaiYang/image/picgobanner.png
summary: (可能有的人用过一些在线网站免费开放的图床。同时也担忧这些免费的图床什么时候会不给你用？)通过github上面的仓库创建一个属于自己的图床。
---

## 首先进入github下载picgo安装包

[picgo的GitHub仓库地址]

[picgo的GitHub仓库地址]: https://github.com/Molunerfinn/PicGo	"picgo的GitHub仓库地址"

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/找picgo下载地址.png)

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/下载picgo.png)

## 安装完成后先用github创建并设置一个用来存放图片的仓库

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/创建仓库.png)

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/创建完成仓库.png)

### 打开picgo软件点击图床设置点击GitHub图床

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/picgo的github设置.png)

#### 强烈建议设定自定义域名（可以解决上传时网络是代理状态。用别的设备（无代理）无法加载图片问题）

使用免费的cdn，格式为：https://cdn.jsdelivr.net/gh/用户名/仓库名

#### 然后进入github添加token

点击这个链接直接跳转https://github.com/settings/tokens

#### 设置步骤如下

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/创建token1.png)

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/创建token2.png)

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/创建token3.jpg)

将token填写到picgo的github设置里面就ok了。

## 可以开始快乐的使用自己的图床了。。

![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/上传.png)



![](https://cdn.jsdelivr.net/gh/JiakaiYang/image/图片操作.png)

如果真的有什么强迫症要删干净的话，可以进入自己的仓库进行删除图片:dog:

## [picgo手册]

[picgo手册]: https://picgo.github.io/PicGo-Doc/zh/guide/config.html#github%E5%9B%BE%E5%BA%8A

