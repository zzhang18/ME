---
title: 初见Luckysheet
date: 2020-12-24 13:20:00 Z
categories:
- learning
tags:
- utilities
- office
last_modified_at: 2020-01-04 13:20:00 Z
layout: post
---

# 简介

🚀Luckysheet ，一款纯前端类似excel的在线表格，功能强大、配置简单、完全开源。

# Demo测试网页

[LuckysheetTrial with import and export](https://zzhang18.github.io/sgb/LuckySheetTrial)

# Luckysheet 适配Excel
* 单元格大小适配（像素）
  * Luckysheet 默认         
    * "defaultRowHeight": 19, //自定义行高
    * "defaultColWidth": 73, //自定义列宽
  * Excel 默认
    * "height": 20, //自定义行高 15
    * "width": 64, //自定义列宽 8.43 
  * exceljs 默认
    * defaultRowHeight	15	Default row height
    * defaultColWidth	(optional)	Default column width
* 适配思路
  * 新建sheet时将表格自定义大小为Excel默认长宽
  * 导入按照文件长宽
  * 导出按照目前表内定义长宽

# 参考资料

* [Luckysheet](https://github.com/mengshukeji/Luckysheet)
* [luckysheet-vue-importAndExport](https://github.com/oy-paddy/luckysheet-vue-importAndExport)
