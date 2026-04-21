# Swap Any Color

**Precise color replacement · no signup · no upload**

A fully client-side tool to replace any color in an image with another color. Everything runs in your browser — your image never leaves your machine.

🔗 **Live tool:** [buildthisnextonline.github.io/swap-any-color/swap-any-color.html](https://buildthisnextonline.github.io/swap-any-color/swap-any-color.html)

---

## What it does

Upload any PNG, JPG, or WebP image, pick a source color and a target color, and replace it — precisely and losslessly. Output is always a PNG at the original resolution with no resampling or quality loss.

---

## Features

- **Region Analyzer** — drag a box over any part of the image to sample the spread of color shades across those pixels. Automatically recommends a tolerance value so you don't have to guess.
- **Single Pixel mode** — click any pixel to sample its exact color. Best for lossless images with flat colors.
- **Tolerance control** — widens the net of source pixels matched for replacement. Has no effect on the target color — every matched pixel gets the exact same target color.
- **Feather edges** — blends boundary pixels gradually instead of cutting sharply, producing a smooth natural-looking edge.
- **Before / After toggle** — compare the original and the result at the same zoom level. Press `B` to toggle.
- **Zoom and pan** — scroll to zoom, Space+drag to pan. FIT button fits the image to the available canvas.
- **Draggable sidebar** — resize the sidebar to your preference.
- **No signup. No upload. No ads.**

---

## How to use

1. Drop or click to upload an image
2. Switch to **Region Analyzer** (recommended for most images)
3. Drag a selection box over the color region you want to replace
4. Click **Apply suggested tolerance** to set the right threshold automatically
5. Pick your target color using the color picker or hex input
6. Click **Replace color**
7. Use Before/After to check the result — adjust tolerance and re-apply if needed
8. Click **Download PNG** to save

### Replacing multiple colors in one image

Each session handles one source color at a time. To replace multiple colors: replace the first color, download the result, reload the downloaded image, and replace the next color.

---

## Why not GIMP or an online tool?

GIMP's color replacement workflow is unintuitive for this specific task. Online tools almost always require signup. This tool does one thing, does it well, runs entirely in your browser, and asks for nothing in return.

---

## Technical notes

- Output is always lossless PNG regardless of input format
- Tolerance maps 0–100 to the full RGB color distance range (0–441)
- Region Analyzer samples pixels across the selected area, computes the average color and maximum spread, and suggests a tolerance that covers the full range with a 20% buffer
- All processing happens via the Canvas API — no server, no external dependencies except Google Fonts

---

## License

MIT — do whatever you want with it.
