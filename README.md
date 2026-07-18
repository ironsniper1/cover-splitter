# Cover Splitter

Split scanned game/DVD/CD **case cover wraps** into separate **back**, **spine**, and **front** images — and crop **disc labels** to a transparent PNG.

Single HTML file. No install, no dependencies, no server. Double-click it and it opens in your browser. Images never leave your computer.

**[▶ Open the tool](https://ironsniper1.github.io/cover-splitter/)**

---

## Why

Scanning a cover wrap gives you one wide image containing the back, spine, and front all at once, usually with scanner margin around the edges and often a little crooked. This cuts it into the three pieces you actually want, at full resolution, with the cut lines placed exactly where you say.

Auto-detection was tried and removed — on real scans the "obvious" fold line is frequently a design element rather than the actual crease, so every cut here is placed by hand with live feedback.

## Features

### Case mode
- **Manual fold lines** — drag the left/right spine folds, type exact pixel values, or nudge with ± buttons and arrow keys (Shift = ×10)
- **Edge trim on all four sides** — top, bottom, left, right, each independently **disable-able**
- **Optional split** — turn the spine split off to export the sheet as a single cover
- **Mirror** — for wraps laid out front | spine | back
- **Live panel preview** that follows the line you're dragging, plus a full preview strip below

### Disc mode
- Circular crop with an **outer disc circle** and a **hub hole**, positioned and sized **independently** of each other
- Exports a PNG with transparency outside the disc and through the center hole
- Hub punch can be disabled for a solid disc

### Both modes
- **Rotation** for crooked scans — 0.01° precision with smooth live feedback, plus 90° quarter turns
- **Presets** — save fold/circle setups and apply them to any later scan; stored as proportions so they work at *any* image size. Persist between sessions, and can be exported/imported as JSON
- **Download individually or all at once**, always at full source resolution
- **Formats** — PNG, JPEG, BMP, and **TIFF** (TIFF decoding is bundled, so it works in Chrome/Edge, not just Safari)

## Usage

1. Open `index.html` (or use the hosted link above)
2. **Open scan…** or drag a scan onto the window
3. Pick **Case** or **Disc**
4. Straighten with the rotate slider if needed
5. Place the lines / circles — drag handles, type values, or use ± and arrow keys
6. **Export all**, or download a single panel

Optionally name and **Save** the setup as a preset to reuse on the rest of a batch.

### Tips
- Front and back panels on a real case are close to equal width — a lopsided split usually means a fold line is in the wrong place
- The first export may prompt Chrome/Edge to "allow multiple downloads" (it saves three files)
- Multi-page TIFFs load page 1; JPEG-compressed TIFFs may not decode — re-save as standard TIFF or PNG

## Hosting it yourself

It's one file with no build step:

```bash
git clone https://github.com/ironsniper1/cover-splitter.git
```

Open `index.html` directly, or enable **GitHub Pages** (Settings → Pages → deploy from branch, root) to serve it.

## Browser support

Chrome, Edge, Firefox, and Safari, on Windows, macOS, and Linux. Everything runs client-side; there is no upload and no network access at runtime.

## License

MIT

---

Made by [VTSTech](https://github.com/ironsniper1)
