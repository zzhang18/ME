---
layout: post
title:  "多语言数据库设计模式"
date:   2020-12-21 11:20:32 +0800
categories: jekyll update
---

# 定义
- 国际化 Internationalization(I18N)：使软件拥有多种语言界面，并未产生实质性变化
- Localization(L10N)： 将软件适应当地的语言并融入本地元素，会对内容有所修改。本地化不仅仅是翻译内容，还有变更单位制式等。

# 数据库设计
## 分栏式
- product_en
- product zh
## 分表式
- en.js
- zh.js
## 翻译表式
- zh - product 
- en - product
## 独立翻译表文件


