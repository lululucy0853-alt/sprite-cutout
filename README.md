<!-- Language: **English** · [中文](README.zh-CN.md) -->

# Sprite Cutout ✂️🔲

**English** · [中文](README.zh-CN.md)

**A zero-install, single-file browser tool for game-UI / sprite work: batch-trim transparent edges + visualize & export 9-slice — all offline, nothing uploaded.**

![license](https://img.shields.io/badge/license-MIT-c9a227)
![build](https://img.shields.io/badge/build-none·single%20HTML-2a9d8f)
![deps](https://img.shields.io/badge/dependencies-zero-8888aa)

---

## ✨ Features

### ✂️ Trim transparent edges
Batch-trim by the alpha bounding box: cut away the transparent border around a sprite. **Pick a folder** → results are written back to a `_trimmed` subfolder (Chrome/Edge, via the File System Access API); or **drag & drop images** → downloaded one by one. Options: padding, alpha threshold. Auto-skips fully-transparent / no-alpha / already-tight images.

### 🔲 9-slice preview
Drag the guide lines to set the 9-slice borders, preview stretching at any target size (corners stay crisp, edges stretch one-way, center stretches both ways). Export the 9 slices as PNG, or copy the border values in Unity / CSS / Cocos formats.

## 🚀 Quick start

Just open **`index.html`** in a browser (Chrome / Edge recommended). No install, no build, no server. → Full guide: **[docs/USAGE.md](docs/USAGE.md)**

## 🔒 Privacy

100% client-side. Images are processed in your browser and **never uploaded** anywhere.

## 🛠 Tech

Single self-contained HTML file · vanilla JS + Canvas + File System Access API · zero dependencies · works fully offline.

> **Browser support**: "Pick a folder" batch-write needs a Chromium browser (Chrome / Edge). Drag-drop + download works everywhere.

## 📚 Docs

- [Usage guide](docs/USAGE.md) · [中文使用文档](docs/USAGE.zh-CN.md)
- [Development log](docs/DEVLOG.md)

## 📄 License

[MIT](LICENSE) © 2026 wanglu
