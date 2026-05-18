# 清风徐来 — Personal Blog

A minimal Jekyll blog deployed on GitHub Pages.

## 部署步骤

### 1. 创建 GitHub 仓库

1. 登录 GitHub（没有账号的话先注册）
2. 点右上角 **+** → **New repository**
3. 仓库名填 `你的用户名.github.io`（比如 `jiyue.github.io`）
4. 选 **Public**
5. 不要勾选任何初始化选项（no README, no .gitignore）
6. 点 **Create repository**

### 2. 上传博客文件

把这个文件夹里的所有内容推送到刚创建的仓库：

```bash
cd blog
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入仓库 → **Settings** → 左侧 **Pages**
2. Source 选 **GitHub Actions**
3. 等 1-2 分钟，访问 `https://你的用户名.github.io` 就能看到博客了

### 4. 写新文章

在 `_posts/` 文件夹里新建文件，命名格式：

```
YYYY-MM-DD-文章标题.md
```

文件开头加上：

```yaml
---
layout: post
title: "你的文章标题"
date: 2026-05-18
tags: [标签1, 标签2]
lang: zh          # zh 或 en
---

正文从这里开始，用 Markdown 写。
```

写完后：

```bash
git add .
git commit -m "new post: 文章标题"
git push
```

推送后等 1-2 分钟，网站自动更新。

## 自定义

- **站点信息**：编辑 `_config.yml` 里的 title、description
- **关于页面**：编辑 `about.md`，把邮箱换成你自己的
- **样式调整**：编辑 `assets/css/main.css`

## 可选：绑定自定义域名

如果你想用自己的域名（比如 `jiyue.me`）：

1. 在域名商那里添加 CNAME 记录，指向 `你的用户名.github.io`
2. 在仓库根目录创建 `CNAME` 文件，内容写你的域名
3. 在 GitHub 仓库 Settings → Pages 里填写自定义域名
