# Sprite Cutout ✂️🔲

**A zero-install, single-file browser tool for game-UI / sprite work: batch-trim transparent edges + visualize & export 9-slice — all offline, nothing uploaded.**

**零安装、单文件的浏览器切图工具：批量裁透明边 + 9-slice 九宫格可视化与导出 —— 全程离线、图片不上传。**

![license](https://img.shields.io/badge/license-MIT-c9a227)
![build](https://img.shields.io/badge/build-none·single%20HTML-2a9d8f)
![deps](https://img.shields.io/badge/dependencies-zero-8888aa)

---

## ✨ Features / 功能

### ✂️ Trim transparent edges / 裁透明边
- **EN** — Batch-trim by the alpha bounding box: cut away the transparent border around a sprite. **Pick a folder** → results are written back to a `_trimmed` subfolder (Chrome/Edge, via the File System Access API); or **drag & drop images** → downloaded one by one. Options: padding, alpha threshold. Auto-skips fully-transparent / no-alpha / already-tight images.
- **中文** — 按 alpha 包围盒批量裁剪，去掉精灵四周的透明留白。**选文件夹** → 裁好写回 `_trimmed` 子文件夹（Chrome/Edge，用 File System Access API）；或**拖入图片** → 逐个下载。可调留边、透明阈值；自动跳过 全透明 / 无透明通道 / 已紧贴 的图。

### 🔲 9-slice preview / 9-slice 九宫格
- **EN** — Drag the guide lines to set the 9-slice borders, preview stretching at any target size (corners stay crisp, edges stretch one-way, center stretches both ways). Export the 9 slices as PNG, or copy the border values in Unity / CSS / Cocos formats.
- **中文** — 拖动分割线设定九宫格边距，任意目标尺寸实时预览拉伸（四角不变形、四边单向拉伸、中心双向拉伸）。导出九块 PNG，或复制 Unity / CSS / Cocos 格式的边距数值。

## 🚀 Quick start / 快速开始

**EN** — Just open **`index.html`** in a browser (Chrome / Edge recommended). No install, no build, no server. → Full guide: **[docs/USAGE.md](docs/USAGE.md)**

**中文** — 直接用浏览器打开 **`index.html`**（推荐 Chrome / Edge）。无需安装、构建或服务器。 → 完整使用文档：**[docs/USAGE.md](docs/USAGE.md)**

## 🔒 Privacy / 隐私

**EN** — 100% client-side. Images are processed in your browser and **never uploaded** anywhere.

**中文** — 纯前端处理，图片只在你本地浏览器里处理，**绝不上传**。

## 🛠 Tech / 技术

Single self-contained HTML file · vanilla JS + Canvas + File System Access API · zero dependencies · works fully offline.

单个自包含 HTML 文件 · 原生 JS + Canvas + File System Access API · 零依赖 · 完全离线可用。

> **Browser support / 浏览器支持**: "Pick a folder" batch-write needs a Chromium browser (Chrome / Edge). Drag-drop + download works everywhere. / 「选文件夹」批量写回需 Chromium 内核浏览器（Chrome / Edge）；拖拽 + 下载所有浏览器通用。

## 📚 Docs / 文档

- [Usage guide / 使用文档](docs/USAGE.md)
- [Development log / 开发日志](docs/DEVLOG.md)

## 📄 License / 许可

[MIT](LICENSE) © 2026 wanglu
