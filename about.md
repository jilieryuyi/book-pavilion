---
layout: book
title: 关于本站
permalink: /about.html
tags: ["说明"]
---

<div class="qr-float">{% include qr.html %}</div>


# 关于本站

这是一个用 **GitHub Pages + Jekyll** 搭起来的静态书库站，没有任何后端、没有数据库，全部内容都是 Markdown 文件，仓库一提交，GitHub 自动构建成网页。

## 内容结构

- 每一类书对应一个目录，目录里有一篇同名 `.blog.md` 文章
- 文章开头是 Jekyll 的 front matter（`title` / `date` / `tags`），下面是该类书的简介和书目清单
- 首页目录与统计数字由 `_data/books.json` 驱动，新增目录后重新生成一次即可

## 怎么加新的一类书

1. 新建目录 `新书名\`，里面放 `新书名.blog.md`
2. 文件头写：

```yaml
---
title: "新书名"
date: 2026-11-26
tags: ["中医", "古籍"]
---
```

3. 正文第一段写简介，之后可以用 `# 文件名` 逐条列书目
4. 重新生成索引数据后提交仓库，GitHub 会自动发布

## 说明

本站只做目录整理与版本索引，不提供书籍下载。所有内容用于查阅、对照与学习。
