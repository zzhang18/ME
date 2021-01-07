---
title: 多语言数据库设计模式
date: 2020-12-21 03:20:32 Z
categories:
- jekyll
tags:
- i18n
- idea
layout: post
---

# 定义
- 国际化 Internationalization(I18N)：使软件拥有多种语言界面，并未产生实质性变化
- Localization(L10N)： 将软件适应当地的语言并融入本地元素，会对内容有所修改。本地化不仅仅是翻译内容，还有变更单位制式等。

# 数据库设计
## 1.分栏式
### 描述
在同一数据栏中加入不同语言的翻译，例如：

* Store
> * id
> * location_en: Shanghai
> * location_zh: 上海

* Product
> * id
> * brand_en: Dyson
> * brand zh: 戴森
### 优点
* 易实现
* 调取不复杂
### 缺点
* 扩展灵活性差
* 调取函数随语言数量增加
### 应用场景
* 小型项目
* 稳定的语言库
## 独立语言翻译表
### 描述
将每项要翻译的内容专门存到对应的表中，里面每一栏对应相应的语言

* Store
> * id
> * location
> * location_translation_id

* Product
> * id
> * brand
> * brand_translation_id

* Translation_Store
> * id
> * en
> * zh


### 优点
* 可应用于已存在数据的模型中
* 每次新加语言只需添加一栏数据
### 缺点
* 需要调整数据模型
* 可能会产生NLL栏
* 查询复杂度增加
### 应用场景
* 已有数据的模型加语言库
## 独立语言栏翻译表式
### 描述
类似于独立语言翻译表，这种是将相同语言的内容存到独立的表下

* Store
> * id
> * location
> * location_translation_id

* Product
> * id
> * brand
> * brand_translation_id

* Translation_Store
> * id
> * en
> * zh

* Translation_Product
> * id
> * en
> * zh

### 优点
* 易于调取
* 模型好调整
* 查询复杂度稍微减轻

### 缺点
* 相对高的存储节点
* 存储大量翻译表

### 应用场景
* 需要独立管理语言表数据库的项目

## 独立翻译表层区域和非翻译区域
### 描述
通过是否需要翻译将数据模型内容分别处理

* Store
> * id
> * number

* Store_Translation
> * id
> * location_translation_id

* Product
> * id
> * total

* Product_Translation
> * id
> * brand_translation_id

* Translation
> * id
> * en
> * zh

### 优点
* 简单调用不需要翻译的字段
* 容易调取译文
* 语言库容易整合
### 缺点
* 表单数据结构复杂

### 应用场景
* 大型复杂的语言数据库项目


# 参考资料
[Database Internationalization(I18N)/Localization(L10N) design patterns](https://medium.com/walkin/database-internationalization-i18n-localization-l10n-design-patterns-94ff372375c6)