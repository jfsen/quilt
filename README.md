# Quilt

**Create beautiful image collages right in your browser.** Quilt is a single-file, zero-dependency HTML application that lets you arrange images into custom-sized collages with multiple layout algorithms, interactive cropping, and high-resolution export.

![Preview](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/badge/license-GPLv3-blue)

---

## Features

- **Multiple Layouts** — Choose from four distinct collage styles:
  - **Equal Grid** — Automatically picks the best-fit grid (rows × columns) based on your images' aspect ratios.
  - **Priority-Weighted Grid** — Uses a squarified treemap algorithm to distribute space proportionally to each image's priority.
  - **Horizontal Strip** — All images in a single row, widths scaled by priority.
  - **Vertical Strip** — All images in a single column, heights scaled by priority.
- **Priority Sliders** — Fine-tune how much space each image gets in priority-based layouts.
- **Drag & Drop Reordering** — Rearrange images by dragging them in the sidebar list.
- **Interactive Cropping** — Click any cell in the collage, then drag to adjust how the image is framed within its cell. Crop hints show which direction is available.
- **Export at Full Resolution** — Download your collage as **PNG** (lossless) or **JPEG** (smaller file) at the exact canvas dimensions you chose — no resolution limits.
- **Custom Canvas Size** — Set your canvas from 200×200 up to 8000×8000 pixels.
- **Keyboard Shortcuts** — Fine-tune crops with arrow keys, reset with `R`, deselect with `Escape`.

---

## Getting Started

1. Open `index.html` in any modern browser.
2. Click **Import Images** and select one or more images.
3. Adjust the canvas size and layout to your liking.
4. Drag images to reorder, and use the priority sliders to control sizing.
5. Click a cell in the preview and drag to crop the image within its cell.
6. Click **Download Collage** to save the result.

That's it — no installation, no server, no dependencies.

---

## Layouts Explained

| Layout | Description |
|---|---|
| **Equal Grid** | Every image gets an equal-sized cell. The algorithm picks the grid (e.g. 2×3 vs 3×2) that best matches the average aspect ratio of your images, minimizing empty cells. |
| **Priority-Weighted Grid** | Space is divided using a squarified treemap algorithm. Each image's cell area is proportional to its priority value, while preserving the image order and keeping cells as square as possible. |
| **Horizontal Strip** | All images sit in one horizontal row. Each image's width is proportional to its priority relative to the total. |
| **Vertical Strip** | All images sit in one vertical column. Each image's height is proportional to its priority. |

---

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `←` `→` `↑` `↓` | Nudge crop of the selected cell (1 pixel per step) |
| `Shift` + arrow keys | Nudge crop by 5 pixels |
| `R` | Reset crop to center for the selected cell |
| `Escape` | Deselect the active cell |

---

## Export Format

- **PNG** — Lossless, best for preserving detail and transparency. Default option.
- **JPEG** — Smaller file size. Best for sharing.

Select your preferred format in the sidebar before downloading.

---

## Technical Details

Quilt is **a single HTML file** with all CSS and JavaScript inlined. There are zero external dependencies, build steps, or server requirements. Just open it and use it.

Works in all modern browsers (Chrome, Firefox, Safari, Edge).

---

## License

This project is licensed under the **GNU General Public License v3**. See [LICENSE](LICENSE) for details.
