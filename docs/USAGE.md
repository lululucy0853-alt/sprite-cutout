# Usage Guide / 使用文档

> Sprite Cutout has two tabs — **✂️ Trim transparent edges** and **🔲 9-slice**. Switch with the tabs at the top.
> Sprite Cutout 有两个标签页 —— **✂️ 裁透明边** 和 **🔲 9-slice**，用顶部标签切换。

---

## 0. Opening / 打开

**EN** — Download the repo (or just `index.html`) and **double-click `index.html`** to open it in your browser. Chrome or Edge is recommended for the "pick a folder" batch feature. Nothing is installed; everything runs locally.

**中文** — 下载仓库（或单独下 `index.html`），**双击 `index.html`** 用浏览器打开。推荐用 Chrome / Edge（「选文件夹」批量功能需要）。无需安装，全部本地运行。

---

## 1. ✂️ Trim transparent edges / 裁透明边

Cut away the transparent border around a sprite so the image sits tight to its content.
去掉精灵四周的透明留白，让图片紧贴内容边缘。

### Three ways to feed images / 三种喂图方式
| Way / 方式 | What happens / 结果 |
|---|---|
| **Pick a folder / 选文件夹** | Picks a folder, trims every image in it, writes results into a `_trimmed` subfolder — originals untouched. *(Chrome/Edge only.)* / 选一个文件夹，裁掉里面每张图，结果写进 `_trimmed` 子文件夹，不动原图。（仅 Chrome/Edge） |
| **Pick images / 选图片** | Pick one or more images; each trimmed result is downloaded. / 选一张或多张图，裁好逐个下载。 |
| **Drag & drop / 拖拽** | Drag images onto the drop zone; same as "Pick images". / 把图片拖到虚线区，效果同「选图片」。 |

### Options / 选项
- **Padding / 留边** — keep N transparent pixels around the content after trimming. / 裁完后四周保留 N 像素透明边。
- **Threshold / 阈值** — alpha ≤ this value counts as transparent. Raise it (e.g. 10) to also cut soft feathered edges. / alpha ≤ 此值算透明；调大（如 10）可连半透明羽化边一起裁。

### Auto-skipped / 自动跳过
Fully-transparent images, images with no alpha channel, and images already tight to their edges. / 全透明的图、没有透明通道的图、已经紧贴边缘的图。

### Result list / 结果列表
Each row shows a thumbnail + `original → trimmed` size (or the skip reason). / 每行显示缩略图 + `原尺寸 → 裁后尺寸`（或跳过原因）。

---

## 2. 🔲 9-slice / 九宫格

Make stretchable borders / panels where corners never distort (rounded corners, strokes stay crisp).
做拉伸不变形的边框 / 面板（圆角、描边不会被拉糊）。

### Steps / 步骤
1. **Load an image / 载入图片** — "Load image…" or drop an image into the window. There's a sample to start with. / 「载入图片…」或把图拖进窗口；打开就有示例图。
2. **Set the borders / 设分割线** — drag the four gold guide lines, or type the left/right/top/bottom border pixels. / 拖动四条金线，或直接填 左/右/上/下 边距像素。
3. **Preview the stretch / 看拉伸** — drag the target width/height sliders; the preview shows the 9-slice result. / 拖目标宽/高滑块，预览区显示九宫格拉伸效果。
4. **Export / 导出**:
   - **Copy border values / 复制边距数值** — one click gives you the four numbers in Unity / CSS formats. / 一键拿到 Unity / CSS 格式的四个数。
   - **Export 9 slices / 导出九块 PNG** — for engines that need the nine images (`tl/tc/tr/ml/mc/mr/bl/bc/br`). / 给需要九张图的引擎。

### Border formats / 边距怎么填进引擎
- **Unity** Sprite Border: `L, B, R, T` (left, bottom, right, top) / 左下右上
- **CSS**: `border-image-slice: T R B L` + `border-width`
- **Cocos scale9 / Laya**: the four inset values directly / 四个 inset 数值直接填

---

## 3. Notes / 说明

- **Privacy / 隐私** — everything runs in your browser; images are never uploaded. / 全部本地运行，图片绝不上传。
- **"Pick a folder" needs Chrome/Edge** — it uses the File System Access API. On other browsers, use "Pick images" / drag-drop instead. / 「选文件夹」依赖 File System Access API，仅 Chrome/Edge；其它浏览器请用「选图片」/ 拖拽。
- **Formats / 格式** — PNG / WebP / TGA / TIFF (anything with an alpha channel). / 支持带透明通道的 PNG / WebP / TGA / TIFF。
