# Neon Chaos Game

Interactive chaos game fractal generator — the classic Sierpinski gasket and beyond.

The chaos game: start at a random point, repeatedly pick one of N polygon vertices, and jump halfway toward it. After many iterations, a fractal attractor emerges. With a triangle (N=3) and ratio 0.5 you get the Sierpinski triangle; other ratios and vertex counts produce related fractals.

Controls:
- **Vertices** — number of polygon corners (3–6)
- **Ratio** — jump fraction (0.3–0.8). Classic Sierpinski uses 0.5.
- **Speed** — points plotted per frame
- **Glow** — neon bloom
- **Color mode** — three neon palettes
- **Randomize vertices** — new random polygon vertex positions
- **Reset** — restore defaults (triangle, ratio 0.5, speed 5)
- **Clear** — clear all points
- **Pause/Resume**

Stats: point count, identified attractor type.

---

Built with vanilla HTML/CSS/JS — Canvas 2D incremental plotting with semi‑transparent background cleared each frame to avoid infinite canvas growth, but points accumulate in buffer; actual drawing happens per frame without clearing to build pattern.

Wait — actually I use `fillRect` per point without clearing background, so points persist. That's fine.

Live demo: https://kiloooai.github.io/neon-chaos-game/
