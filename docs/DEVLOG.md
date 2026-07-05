# Development Log / 开发日志

> Why this tool exists and how it took shape. / 这个工具为什么做、怎么一步步长成的。

---

## Origin / 起源

**EN** — Two chores kept eating time in day-to-day game-UI work: (1) trimming the transparent border off exported sprites, and (2) building 9-slice borders. Both are simple but repetitive. The goal: shrink the busywork so time goes to judgment and design, not pixel-pushing.

**中文** — 游戏 UI 日常里有两件反复耗时间的琐事：① 给导出的精灵裁掉四周透明边；② 做 9-slice 九宫格。都简单但重复。目标：把这类杂活压掉，让时间留给判断与设计，而不是搬像素。

---

## v1.0.0

### Milestones / 里程碑

**1. Trim, first as a Python script / 裁透明边，先做成 Python 脚本**
- EN — Started as a Pillow script (`alpha` bounding-box crop) + a drag-onto `.bat` for non-terminal use. Fast for whole folders.
- 中文 — 最初是 Pillow 脚本（按 alpha 包围盒裁）+ 一个拖拽 `.bat`（不用敲命令行）。整文件夹批处理很快。

**2. 9-slice as a standalone web tool / 9-slice 做成独立网页**
- EN — A single HTML: drag guide lines, live-preview the stretch on a canvas, export the nine slices / border numbers. Verified the nine-slice math with headless screenshots (rounded corners must not distort).
- 中文 — 一个单文件 HTML：拖分割线、canvas 实时预览拉伸、导出九块 / 边距数值。用无头截图核实九宫格数学（圆角不能拉糊）。

**3. Integrated into one tool / 集成成一个工具**
- EN — Merged both into a single `index.html` with a tab switch. The trim feature was re-implemented in the browser (Canvas + File System Access API) so a folder can be picked and results written back to a `_trimmed` subfolder — no Python, no install. Drag-drop / download is the fallback where the API isn't available.
- 中文 — 合并成单个带标签切换的 `index.html`。裁透明边改用浏览器实现（Canvas + File System Access API），可以选文件夹、把结果写回 `_trimmed` 子文件夹 —— 不装 Python、零安装。不支持该 API 时回退到拖拽 / 下载。

### Design decisions / 设计决策

- **EN — Single self-contained HTML.** No build step, no dependencies, no server. Double-click and it works, forever, offline. Easiest thing to keep alive and to share.
- **中文 — 单个自包含 HTML。** 无构建、零依赖、无服务器。双击就能用，离线永久有效。最好维护、最好分享。

- **EN — Client-side only.** Images never leave the browser. For game art this also matters for confidentiality.
- **中文 — 纯前端。** 图片不离开浏览器。对游戏美术，这也关乎保密。

- **EN — Verify with numbers, not eyeballs.** During development the trim/9-slice logic was checked with headless runs that assert exact pixel results (e.g. `200×200 → 80×60, offset 60,70`), because a screenshot can look right while the data is wrong.
- **中文 — 靠数字验证，不靠肉眼。** 开发时用无头运行断言精确像素结果（如 `200×200 → 80×60，偏移 60,70`）——截图可能"看着对"但数据是错的。

### Known limits / 已知限制

- EN — "Pick a folder" batch-write requires a Chromium browser (File System Access API). Elsewhere, use drag-drop + per-file download.
- 中文 — 「选文件夹」批量写回需 Chromium 内核（File System Access API）；其它浏览器用拖拽 + 逐个下载。

---

## Roadmap / 后续设想

- EN — Optional English UI toggle; batch 9-slice; remember last settings.
- 中文 — 可选的英文界面切换；批量 9-slice；记住上次设置。
