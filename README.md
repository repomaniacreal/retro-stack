# 🧱 Retro Stack

An isometric block-stacking game with a retro/arcade theme (neon colors, CRT scanlines, pixel font). Built purely with **HTML, CSS, and JavaScript** — no libraries or build tools required.

## 📦 Package Contents

```
index.html   # the entire game (HTML + CSS + JS in a single file)
README.md    # this file
```

## ⚙️ Installation

No installation needed. Pick one of the following:

1. **Open it directly**
   Double-click `index.html`, or drag it into your browser window (latest Chrome/Edge/Firefox/Safari).

2. **Run it via a local server (optional, recommended for mobile testing)**
   ```bash
   # from the folder containing index.html
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000/index.html` in your browser.

3. **Upload to static hosting**
   Since everything is self-contained in a single HTML file, you can upload it directly to GitHub Pages, Netlify, Vercel, or any other static host. Because the file is named `index.html`, it will be served automatically as the site's homepage.

> An internet connection is needed to load the *Press Start 2P* font from Google Fonts. If offline, the game still runs but falls back to a generic monospace font.

## 🎮 How to Play

1. The first block is already placed in the center as the foundation.
2. A second block slides back and forth automatically.
3. **Click / tap the screen, or press the Spacebar** right when the moving block is aligned with the block below it.
4. Any part that doesn't overlap (the overhang) gets sliced off and falls away.
5. Each successfully stacked block = +1 score, and the next block moves slightly faster.
6. If the block misses completely (no overlap at all) → **Game Over**.
7. Press **MAIN LAGI** (Play Again) to restart.

## 🕹️ Controls

| Action | Input |
|---|---|
| Place block | Mouse click / Screen tap / Spacebar |
| Restart after losing | On-screen "MAIN LAGI" button |

## 🏆 Scoring

- **Score**: number of blocks successfully stacked in the current run.
- **Best**: your highest score, saved automatically in the browser (`localStorage`), so it persists across visits unless site/browser data is cleared.

## 🛠️ Quick Customization

Everything can be adjusted directly inside `index.html`:

- **Theme colors**: edit the values in `:root { --bg1; --bg2; --accent; --accent2; --ink; }`, and the `PALETTE` array in the JavaScript section for block colors.
- **Block height**: edit the `BLOCK_H` constant.
- **Starting speed & speed ramp**: edit `speed` and the formula `speed = Math.min(7, 2.2 + score*0.12)`.
- **Movement range of the sliding block**: edit the `range` variable (default `130`).

## 💻 Compatibility

Works in modern browsers (Chrome, Edge, Firefox, Safari), latest versions, on both desktop and mobile. No Node.js, npm, or external dependencies required besides the optional Google Fonts connection.

## 📄 License

Free to use, modify, and share for personal or learning purposes.
