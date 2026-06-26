# Scroll-Scrub Showcase

Three premium, scroll-driven landing pages where the hero animation is controlled **frame-by-frame by the user's scroll**. Built for a vibecoding class with plain HTML, CSS and JavaScript — **no frameworks, no dependencies, no build step.**

## 🔗 Live demo

**→ [View the showcase](https://trojanhammer.github.io/vibecoding-demo/)**

| Demo | What it shows | Link |
| --- | --- | --- |
| 🍎 **MacBook Pro** | Scroll-scrubbed product video, light Apple-style theme | [Open](https://trojanhammer.github.io/vibecoding-demo/macbook.html) |
| 👕 **The Summit Tee** | Same technique, warm editorial fashion look | [Open](https://trojanhammer.github.io/vibecoding-demo/shirt.html) |
| 🍚 **Nasi Lemak** | Non-product scroll story (sambal pour) | [Open](https://trojanhammer.github.io/vibecoding-demo/recipe.html) |

## ✨ The technique

Each page pins a hero section to the screen and maps your **scroll position to the video's playback time**, so scrolling scrubs the clip forwards and backwards like a flipbook. When the animation finishes, the page unpins and reveals the rest of the content with on-scroll fade-ins.

- **Scroll-scrub video** — the scroll position drives `video.currentTime` (used on all three pages, with the option to fall back to a live `<canvas>` animation if the video can't load).
- **Title-band layout** — the headline sits in its own clean band above the media so text never fights the product for contrast.
- **On-scroll reveals** — content fades in using `IntersectionObserver`.

## 🧩 Tech

- Vanilla **HTML / CSS / JavaScript** — zero libraries.
- Hosted on **GitHub Pages**.
- Smooth scrubbing relies on the video being served over HTTP (GitHub Pages handles this).

## 📁 Structure

```
index.html      → landing page (menu of all three demos)
macbook.html    → MacBook Pro demo   + mac.mp4
shirt.html      → Summit Tee demo    + shirt.mp4
recipe.html     → Nasi Lemak demo    + foodhero.mp4
```

## 🛠️ Run locally

Because video scrubbing needs HTTP (not `file://`), serve the folder with any static server:

```bash
python3 -m http.server 8000
# then open http://127.0.0.1:8000
```

---

Built with [Claude](https://claude.com/claude-code) for a vibecoding class · 2026
