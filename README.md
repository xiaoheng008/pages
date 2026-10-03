# Xiaoheng 的思考

个人文章站，使用 Hugo 和 [OINK](https://oink.pgsty.com/) 生成，通过 GitHub Pages 发布。文章源文件与网站内容相同：放进 `content/blog/post/` 的文章会随站点公开发布。

## 写一篇文章

在 `content/blog/post/` 新建 Markdown 文件，例如 `my-idea.zh.md`：

```markdown
---
title: 文章标题
date: 2026-10-04
description: 一句话介绍文章。
author: Xiaoheng
tags: [思考]
---

从这里开始写正文。
```

提交并推送到 `main` 后，GitHub Actions 会构建并发布网站。文章没有草稿状态；推送即公开。不要把不准备公开的内容放进 `content/`。

## 本地预览

需要 Git、Go 1.27+ 和 Hugo Extended 0.165.0+：

```bash
hugo server
```

打开 <http://localhost:1313/>。首次运行会下载 `go.mod` 中锁定的 OINK 主题版本。

## 发布设置

仓库的 GitHub Actions 工作流会在 `main` 有新提交时部署到 GitHub Pages。首次发布前，在 GitHub 仓库的 **Settings → Pages** 中把 Source 设为 **GitHub Actions**。本站地址配置为 <https://xiaoheng008.github.io/pages/>。
