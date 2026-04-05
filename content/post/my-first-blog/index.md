---
title: 一点本框架下的md格式注意
date: 2026-04-05T12:00:00+08:00
image: cover.jpg   # 封面图放在同目录下
categories: [教程]
tags: [markdown, hugo]
---

## 第一部分：Markdown 示例

这是一个段落，包含 **粗体** 和 *斜体*。

### 列表示例
- 项目一
- 项目二
  - 子项目

## 第二部分：格式

Front Matter 格式（必须）
每篇博客的 .md 文件开头必须包含如下格式的元数据：

三条-
title: "文章标题"
date: 2026-04-05T12:00:00+08:00   # 日期时间（ISO 8601）
categories: ["分类1", "分类2"]    # 分类（数组）
tags: ["标签1", "标签2"]         # 标签（数组，可选）
image: "cover.jpg"                # 封面图（可选，放在同目录下）
三条-

### 链接和图片
访问 [Hugo 官网](https://gohugo.io) 了解更多。

![图片描述](image.jpg)

## 第三部分：混合 HTML

<div class="note" style="border-left: 4px solid #3498db; padding-left: 1rem;">
  <h4>自定义 HTML 块</h4>
  <p>这里完全使用 HTML，可以添加任何样式或结构。</p>
</div>

## 第四部分：使用 Shortcodes

{{< figure src="/img/demo.jpg" caption="带标题的图片" >}}

## 代码示例

```python
def hello():
    print("Hello, World!")
