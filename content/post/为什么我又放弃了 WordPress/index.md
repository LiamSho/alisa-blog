---
title: "为什么我又放弃了 WordPress"
description: "先是踩坑 WP，再是被打，最后放弃。。。"
date: "2022-08-10 03:30:00+0800"
slug: "why-i-give-up-wordpress"
image: "wordpress-logo.png"
tags:
    - 博客
    - 折腾
---

# 为什么我又放弃了 WordPress

先是踩坑 WP，再是被打，最后放弃。。。

## 各种经历

说实话我搭博客有很大部分原因是处于想要玩一玩。

在最初接触的时候，用的是 WordPress，在一台运行 CentOS 7 的服务器上搭建，使用宝塔 Linux 面板和 LAMP，参考 [小游dalao的博客](https://xiaoyou66.com/archives/1634) 并使用他所制作的主题 kratos 进行搭建。服务器是腾讯云的学生机，部署完之后的结果就是太卡了，主要是网络带宽比较小，当时并没有使用 CDN 来进行加速。

过了一年左右，短暂的使用 Hugo 搭建了一个站点，部署在 Azure Static Web Apps 上。

又过了一年左右，到现在，再一次尝试使用 WordPress，部署在一台运行 Debian 11 的服务器上，使用容器的方式进行部署，使用 Portainer 进行容器的管理，Nginx Proxy Manager 进行反向代理的管理。

现在，这个站点使用 Hugo 制作，部署在 Azure Static Web Apps 上。。。

## 为什么放弃 WordPress

### Oh My God！PHP！

老实说我很不喜欢 PHP 这个语言。我所使用过的所有语言里面，PHP 是最让我感觉不舒服的，语法感觉很怪。

然而最重要的是，这个玩意在部署的时候非常麻烦。

容器技术的诞生缓解了不少 PHP 部署麻烦，环境乱七八杂的问题。但我仍然会遇到在我使用 PHP 时最烦的权限问题。

### [Obsolete] WordPress

WordPress 确实是个成熟的 CMS 系统，但是它的问题实在是太多了。

和大多使用 Node.JS 制作的前端相比，WordPress 由于使用 PHP，相比而言太慢了。WordPress 本身的安全性也是非常差。你确实可以使用 WordPress 搭建一个十分优秀的网站，但是与之相对的，你需要投入额外的精力去管理插件更新，主题更新，WordPress 本体的更新等。还要去处理 WordPress 的安全问题。

对于个人制作一个小博客而言，WordPress 并不是一个很好的选择。

## 为什么使用 SSG

静态网站生成器（SSG）有两个极大的优势。

首先是部署简单，你可以把网站托管比如 GitHub Pages 之类的地方，或者直接放在 CDN。和自己维护一个服务器相比，这实在是太简单了。

其次，因为全是静态内容，全是纯粹的 HTML，CSS，JS，所以站点的速度飞快。

当然，SSG 也有其缺点。最主要的就是内容管理麻烦。WordPress 之类的 CMS 提供了 UI 进行内容管理，也有 API 进行内容的管理。而大多 SSG 需要手动管理内容，元数据以 Front Matter 的模式写在每个文章的前面，不能集中管理。

但是总的来说，对于制作个人博客而言，SSG 能够很好的满足需求。

## 未来？

Who knows?