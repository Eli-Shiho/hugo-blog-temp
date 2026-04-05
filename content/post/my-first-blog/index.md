---
title: 我的第一篇文章
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

### 链接和图片
访问 [Hugo 官网](https://gohugo.io) 了解更多。

![图片描述](image.jpg)

## 第二部分：混合 HTML

<div class="note" style="border-left: 4px solid #3498db; padding-left: 1rem;">
  <h4>自定义 HTML 块</h4>
  <p>这里完全使用 HTML，可以添加任何样式或结构。</p>
</div>

## 第三部分：使用 Shortcodes

{{< alert type="tip" >}}
这是一个使用 shortcode 创建的提示框。
{{< /alert >}}

{{< figure src="/img/demo.jpg" caption="带标题的图片" >}}

## 代码示例

```python
def hello():
    print("Hello, World!")
