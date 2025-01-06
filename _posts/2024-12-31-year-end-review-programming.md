---
title: 2024年终总结：编程篇
---

在互联网行业工作的十几年时间里，我学会很多编程技能 → [feelang#编程技能](https://feelang.xyz/about/#%E7%BC%96%E7%A8%8B%E6%8A%80%E8%83%BD)。

学习这些技能，有的是出于工作需要，有的是出于兴趣爱好。

可是随着技术浪潮的更迭，很多技能早已是明日黄花，失去了价值。

好在我自己创业以后，逐渐了对追求新技术失去了兴趣。

在我看来，只要能快速解决业务问题，它就是好技术。

基于目前的创业需求，我选择了以下技术栈作为主力：

技术栈 | 用途
--- | ---
Flutter | 桌面应用、APP、Web 应用
Django | Web 应用
Python | 小工具、命令行应用
小程序 | 微信生态，提升内容交互性

过去几年，我做了[很多小程序](https://feelang.xyz/weapps/)。随着强制备案政策的推出，好几个我已经不想再继续维护。

目前还想继续优化的是「森罗日语」，25 年应该会加大投入。

另外，Django 是我非常喜欢的 web 框架，25 年应该会往技术社区输出一些内容。

利用以上技术框架，我今年做了不少应用，有大有小，有的半途而废，有的过于粗糙。

只有四个还算能拿得出手：

名称 | 类型 | 技术栈
--- | --- | ---
[地址解析软件](https://github.com/Hefengcloud/residential-address-parsing) | 桌面应用 | Flutter
某基金会网站 | 网站 | Website
[森罗日语CMS](https://github.com/Hefengcloud/senluo_japanese_cms) | 桌面应用 | Flutter
[wafu-cms](https://github.com/Hefengcloud/wafu-cms/tree/main/wafu_cms) | 命令行 | Python

## 地址解析软件

这是一个 Windows 桌面应用，也是我第一次用 Flutter 干这个事儿。

期间当然遇到了不少问题，尤其是 [db 创建失败的问题](https://github.com/Hefengcloud/residential-address-parsing/issues/5)，有点难搞。

这个小软件的主要功能是**解析不规则地址，生成结构化数据**。

所涉及到技术也不难，主要包括：

- Excel文件的读取和写入
    - [如何读取 excel 文件](https://blog.csdn.net/FeeLang/article/details/136925345)
- 数据库操作
- 调用地图API

从最终成品来看，技术并不复杂，但是寻找解决方案的过程可是没少费工夫。

一开始我误以为地图公司的 open api 只支持 web 应用，所以一直在纠结到底要做成不带服务器的桌面应用还是做成 web 应用。

后来偶然发现了一个部署在 github 上的静态网站，用的是 open api。

然后我就用 [Selenium with Python](https://selenium-python.readthedocs.io/) 完成了这个软件的第一版，相当于是个爬虫应用。

后来在 GPT 的帮助下，完成了直接用 Dart 代码调用地图 open api 的功能。

整个过程可谓柳暗花明，一波三折。

## 基金会网站

> WordPress + 腾讯云

- 域名申请
- 服务器备案
- HTTPS 证书
- 运维服务

## 森罗日语CMS

- 仮名
- 文法
	- JLPT语法要点
- 単語
	-  按主题分类的词汇（如饮食、交通、购物等）
- 漢字
	- JLPT 高频字
- 慣用語
	- ことわざ
- オノマトペ
- 表現（未完成）
- 敬語（未完成）

## wafu-cms

> 日语知识的文本处理器

- JLPT 语法要点例句翻译
	- 抽取JLPT 语法要点文件（YAML格式）中的例句，生成 AI 翻译指令
	- 将指令拷贝到 ChatGPT 对话框，生成例句的中文翻译
	- 将中文翻译保存成 yaml 文件，用代码写入所对应的 YAML 文件
- 日语文章排版：
	- 格式化标点符号
		- `“` → `「`
		- `”` → `」`
		- `,` → `，`
		- `?` → `？`
	- 格式化特殊符号
		- `en:` → `◎`
		- `jp:` → `◎`
		- `zh:` → `→`
		- `:` → `：`
	- 为例句中出现的「漢字」添加「振り仮名」
	- 生成目标平台文章
		- 微信公众号
		- [知乎专栏](https://www.zhihu.com/column/everjapan)
		- [网站](https://everjapan.com)
