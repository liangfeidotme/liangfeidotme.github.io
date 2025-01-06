---
title: 2024年终总结：编程篇
---

24年一共做了好几个产品，有的半途而废，有的过于粗糙，能拿得出手的有四个：

名称 | 类型 | 技术栈
--- | --- | ---
[地址解析软件](https://github.com/Hefengcloud/residential-address-parsing) | 桌面应用 | Flutter
某基金会网站 | 网站 | Website
[森罗日语CMS](https://github.com/Hefengcloud/senluo_japanese_cms) | 桌面应用 | Flutter
[wafu-cms](https://github.com/Hefengcloud/wafu-cms/tree/main/wafu_cms) | 命令行 | Python

## 地址解析软件

> 解析不规则地址，生成结构化数据

- Excel文件的读取和写入
- 调用地图API

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
