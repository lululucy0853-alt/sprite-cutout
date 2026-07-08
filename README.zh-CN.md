<!-- Language: [English](README.md) · **中文** -->

# Sprite Cutout ✂️🔲

[English](README.md) · **中文**

**零安装、单文件的浏览器切图工具:批量裁透明边 + 9-slice 九宫格可视化与导出 —— 全程离线、图片不上传。**

![license](https://img.shields.io/badge/license-MIT-c9a227)
![build](https://img.shields.io/badge/build-none·single%20HTML-2a9d8f)
![deps](https://img.shields.io/badge/dependencies-zero-8888aa)

---

## 🌐 在线使用

**在线地址 → https://lululucy0853-alt.github.io/sprite-cutout/**

打开链接直接开切 —— 免安装、免配置。全程本地运行、离线可用,图片绝不上传。

---

## ✨ 功能

### ✂️ 裁透明边
按 alpha 包围盒批量裁剪,去掉精灵四周的透明留白。**选文件夹** → 裁好写回 `_trimmed` 子文件夹(Chrome/Edge,用 File System Access API);或**拖入图片** → 逐个下载。可调留边、透明阈值;自动跳过 全透明 / 无透明通道 / 已紧贴 的图。

### 🔲 9-slice 九宫格
拖动分割线设定九宫格边距,任意目标尺寸实时预览拉伸(四角不变形、四边单向拉伸、中心双向拉伸)。导出九块 PNG,或复制 Unity / CSS / Cocos 格式的边距数值。

## 🚀 快速开始

直接用浏览器打开 **`index.html`**(推荐 Chrome / Edge)。无需安装、构建或服务器。 → 完整使用文档:**[docs/USAGE.zh-CN.md](docs/USAGE.zh-CN.md)**

## 🔒 隐私

纯前端处理,图片只在你本地浏览器里处理,**绝不上传**。

## 🛫 自己部署

就是一个静态 HTML 文件 —— 放到任意静态托管上一分钟搞定。

- **Cloudflare Pages**(推荐):后台 → *Workers & Pages → Create → Pages → 连接 Git* → 选这个仓库 → **构建命令:_留空_**,**输出目录:`/`**。在同一后台加自定义域名即可。
- **GitHub Pages**:仓库 **Settings → Pages → Source:_Deploy from a branch_ → `main` / `(root)`**,上线地址 `https://<用户名>.github.io/sprite-cutout/`。

## 🛠 技术

单个自包含 HTML 文件 · 原生 JS + Canvas + File System Access API · 零依赖 · 完全离线可用。

> **浏览器支持**:「选文件夹」批量写回需 Chromium 内核浏览器(Chrome / Edge);拖拽 + 下载所有浏览器通用。

## 📚 文档

- [中文使用文档](docs/USAGE.zh-CN.md) · [English usage](docs/USAGE.md)
- [开发日志](docs/DEVLOG.md)

## 📄 许可

[MIT](LICENSE) © 2026 wanglu
