# 书库 · GitHub Pages 静态站

Jekyll 站点，GitHub 自动构建，无需本地装 Ruby。

## 目录结构

```
D:\blog
├── _config.yml          站点配置（title / url / baseurl / 布局默认值）
├── _data\books.json     首页索引数据（285 个目录，脚本生成）
├── _layouts\            模板：default（框架）、home（首页）、book（文章页）
├── assets\css\style.css 全站样式
├── index.md             首页（目录卡片 + 搜索）
├── catalog.md           总表（285 行完整清单，带跳转链接）
├── about.md             关于
├── 404.md               404 页
├── 伤寒论\伤寒论.blog.md  每类书一个目录 + 一篇同名文章
└── 金匮要略\...          同上，共 285 个
```

## 发布步骤

1. 仓库 `jilieryuyi/tcm-books.github.io` → Settings → Pages
2. Source 选 **Deploy from a branch**，Branch 选 `master`，目录 `/ (root)`，Save
3. 推送代码后等 1–3 分钟，访问：
   `https://jilieryuyi.github.io/tcm-books.github.io/`

> 因为仓库名不等于 `jilieryuyi.github.io`，属于**项目站点**，所以 `_config.yml` 里
> `baseurl: "/tcm-books.github.io"`。如果把仓库改名成 `jilieryuyi.github.io`，
> 把 baseurl 改成 `""` 即可变成用户站点，直接 `https://jilieryuyi.github.io/` 访问。

## 新增一类书

1. 建目录 `新书名\`，放 `新书名.blog.md`，开头写：

```yaml
---
title: "新书名"
date: 2026-11-26
tags: ["中医", "古籍"]
---
```

2. 正文第一段写简介，之后用 `# 文件名` 逐条列书目
3. 重新生成 `_data\books.json`（或手动加一条记录），提交即自动发布

## 更新索引数据

`_data\books.json` 由脚本扫描各目录的 `.blog.md` 生成，字段：
`title` / `dir` / `url` / `kinds`（品种数）/ `files`（文件数）/ `desc`（简介前 90 字）。
