# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

Vibe Lab 是一个静态网站集合，用于存放阿林 (Wang Runlin) Vibe Coding 产出的 HTML 项目。每个子项目是独立的静态页面或小型 Web 应用。

## 部署目标

- **主要**: GitHub Pages
- **可选**: Vercel, Cloudflare Pages

## 项目结构

```
vibe-lab/
├── [project-name]/     # 每个 Vibe 项目一个文件夹
│   ├── index.html      # 入口文件
│   ├── style.css       # 样式（可选，可内联）
│   └── script.js       # 脚本（可选，可内联）
└── index.html          # 主页，列出所有项目
```

## 技术约定

- **样式**: 倾向使用 Tailwind CSS CDN 或内联样式
- **脚本**: 原生 JavaScript，避免引入重型框架
- **设计风格**: 极简现代，高设计感
- **文件**: 单个 HTML 文件优先（便于分享和部署）

## 常用命令

```bash
# 本地预览（使用任意静态服务器）
npx serve .
# 或
python -m http.server 8000

# 部署到 GitHub Pages（推送到 main 分支后自动部署）
git push origin main
```

## 新项目创建

1. 创建以项目名命名的文件夹
2. 添加 `index.html` 作为入口
3. 更新根目录 `index.html` 的项目列表
