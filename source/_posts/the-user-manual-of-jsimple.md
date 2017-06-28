title: JSimple主题用户指南
date: 2017-04-18 09:49:58
author: 唐先森
avatar: /images/favicon.png
authorLink: https://www.tangkunyin.com
authorAbout: https://about.tangkunyin.com
authorDesc: 一个写代码的「伪文人」
categories: 资源
tags:
	- hexo
	- 网站
keywords: JSimple主题用户指南
description: 这里，我将为大家写一篇早就该写的文档，关于JSimple主题的用户使用指南。如果你下载了这个主题使用中遇到了麻烦和错误，请第一时间阅读本文。当然，主题也在持续优化和改进，本文也将跟进。方便就请保存书签。
photos:
  - /img/2017/hexo-gitpages1.png
---

![hexo-blog-basic](/img/2017/hexo-blog-basic.jpg)

### 本文将持续跟进主题更新，除了Github的文档，就这里更详细了，有错误发现和建议可以直接提在本文后头

> 任何的软件作品，不论是成品还是半成品，提供一份易懂的说明还是很重要也非常有必要的。在这件事情上，我很抱歉！因为主题制作过程本来断断续续，开始我也只是想弄个主题供自己用，后来发到Github和hexo官方，发现还是有不少朋友喜欢，在此一并感谢。最近Github反馈的问题很频繁，所以写个文档显得更为迫切和有必要

### 主题概况

大概介绍下，主题的统计用的`CNZZ`，评论组件用的`Disqus`，搜索是`Google InsightSearch`，大致风格是简书网的前身。对于统计和评论，你可以直接改主题的对应文件，替换就好了，只是考虑到统计和评论信息为私有信息，因此把那两项配置放到了站点配置文件中，如果你为此感到难受，请自己放到主题配置文件里就好。多余的不用纠结。

当你下载了这份主题，改好站点配置后，第一个工作不应该是`hexo g`或`hexo s`运行演示，因为这样你一定会遇到错误，要完整的运行，你需要手动配置如下项目：

#### 1、写作模板文件配置

在`scaffolds`文件夹下，保留两个文件即可：`post.md`和`page.md`，他们分别表示普通文章和独立页面

**post**模板内容如下

```
title: {{ title }}
date: {{ date }}
author: 唐先森
avatar: /images/favicon.png
authorLink: https://www.tangkunyin.com
authorAbout: https://about.tangkunyin.com
authorDesc: 一个写代码的「伪文人」
categories: 技术
tags: 
- 技术
- 还是技术
keywords: 
description: 
photos: 
- img/2017/demo.jpg
---
```

> 如果新建的文章要归属于某个分类，请在`categories`处对应你的分类名称即可。标签使用同理，一篇文章可以有多个标签，打标签的方式就是写成数组方式。`photos`是缩略图，地址可以是相对的，也可以是绝对的。

**page**模板同上，但没有`categories`和`tags`，多了`comments`，后者用来控制独立页是否支持评论组件。至于要把作者的信息放到模板里，是考虑到如果网站采用投稿方式，可以保留原创信息。即：显示不同作者不同文章信息，不会乱！

#### 2、站点分类别名和自定义URL配置

关于自定义URL，请参考这篇文章：[在hexo博客中打造相对完美的URL](https://shuoit.net/tech/build-perfect-url-in-hexo.html)

**分类别名**和**标签别名**配置，站点`_config.yml`文件中，其中主题配置文件里的`menu`项需要和`category_map`键值对一致。二者顺序可以不同，但是主题中的顺序决定网站导航栏菜单的顺序。

```
# Category & Tag
default_category: 技术
category_map:
   技术: tech
   人文: humanity
tag_map:
  hexo: hexo
  生活: life
```

#### 3、到这里，新建的文章写好，就能预览了










