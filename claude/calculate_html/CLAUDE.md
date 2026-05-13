# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

儿童计算题 HTML 生成器 — 生成可直接打印/使用的数学练习题网页。

## Output Convention

- 每次生成的 HTML 文件统一放在 `D:\SynologyDrive\950_CODE\claude\calculate_html/` 目录下
- 文件名格式：`math_{年级}_{题号}.html`，例如 `math_grade1_001.html`
- 每次生成新文件，不要覆盖已有文件

## HTML 规范

- 单个自包含 HTML 文件，不使用外部依赖（CDN、字体、图片等）
- 使用内联 CSS，适合 A4 打印排版
- 中文字体优先使用系统字体（Microsoft YaHei, SimHei, PingFang SC 等）
- 内容一次性渲染完成，不使用 JavaScript
- 所有 HTML 文件生成后需实际写入磁盘

## 题目生成规则

### 题型矩阵

| 题型 | 年级 | 说明 |
|------|------|------|
| 加减法 | 一年级 | 20 以内加减 |
| 加减法 | 二年级 | 100 以内加减，含进退位 |
| 加减法 | 三年级 | 1000 以内加减，三位数 |
| 加减乘除 | 三年级 | 乘法表内乘除、带余数除法 |
| 加减乘除 | 四年级 | 多位数乘除法、四则混合运算 |
| 分数 | 五年级 | 分数加减、通分、约分 |
| 分数 | 六年级 | 分数乘除、分数四则混合 |
| 小数 | 四年级 | 小数加减 |
| 小数 | 五年级 | 小数乘除 |
| 方程 | 六年级 | 一元一次方程 |
| 比/比例 | 六年级 | 化简比、求比值 |

### 排版要求

- 每页约 20-30 题，按列排列
- 数字需留出填写答案的空格/下划线
- 题目排列整齐，对齐
- 字体大小适中（题目 16-20px，标题 24-28px）

## 常用命令

```bash
# 在浏览器中打开最新的 HTML
# Windows: start D:\SynologyDrive\950_CODE\claude\calculate_html\math_grade1_001.html
```
