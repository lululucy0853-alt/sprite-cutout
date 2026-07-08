# Usage Guide

**English** · [中文](USAGE.zh-CN.md)

> Sprite Cutout has two tabs — **✂️ Trim transparent edges** and **🔲 9-slice**. Switch with the tabs at the top.

---

## 0. Opening

Download the repo (or just `index.html`) and **double-click `index.html`** to open it in your browser. Chrome or Edge is recommended for the "pick a folder" batch feature. Nothing is installed; everything runs locally.

---

## 1. ✂️ Trim transparent edges

Cut away the transparent border around a sprite so the image sits tight to its content.

### Three ways to feed images
| Way | What happens |
|---|---|
| **Pick a folder** | Picks a folder, trims every image in it, writes results into a `_trimmed` subfolder — originals untouched. *(Chrome/Edge only.)* |
| **Pick images** | Pick one or more images; each trimmed result is downloaded. |
| **Drag & drop** | Drag images onto the drop zone; same as "Pick images". |

### Options
- **Padding** — keep N transparent pixels around the content after trimming.
- **Threshold** — alpha ≤ this value counts as transparent. Raise it (e.g. 10) to also cut soft feathered edges.

### Auto-skipped
Fully-transparent images, images with no alpha channel, and images already tight to their edges.

### Result list
Each row shows a thumbnail + `original → trimmed` size (or the skip reason).

---

## 2. 🔲 9-slice

Make stretchable borders / panels where corners never distort (rounded corners, strokes stay crisp).

### Steps
1. **Load an image** — "Load image…" or drop an image into the window. There's a sample to start with.
2. **Set the borders** — drag the four gold guide lines, or type the left/right/top/bottom border pixels.
3. **Preview the stretch** — drag the target width/height sliders; the preview shows the 9-slice result.
4. **Export**:
   - **Copy border values** — one click gives you the four numbers in Unity / CSS formats.
   - **Export 9 slices** — for engines that need the nine images (`tl/tc/tr/ml/mc/mr/bl/bc/br`).

### Border formats
- **Unity** Sprite Border: `L, B, R, T` (left, bottom, right, top)
- **CSS**: `border-image-slice: T R B L` + `border-width`
- **Cocos scale9 / Laya**: the four inset values directly

---

## 3. Notes

- **Privacy** — everything runs in your browser; images are never uploaded.
- **"Pick a folder" needs Chrome/Edge** — it uses the File System Access API. On other browsers, use "Pick images" / drag-drop instead.
- **Formats** — PNG / WebP / TGA / TIFF (anything with an alpha channel).
