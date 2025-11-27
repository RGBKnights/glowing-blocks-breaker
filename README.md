# Tiny Breakout (URL Bar Edition)

A tiny Breakout-inspired toy that renders entirely in the browser URL bar. The page itself is minimal; the action happens inside the address bar as the URL rewrites every frame.

## Play

1. Open `index.html` in your browser (or serve the folder with any static file server).
2. Watch the URL bar—three rows of Braille brick glyphs, the ball, and the paddle are drawn as glyphs in the path.
3. Use **←/→** or **A/D** to move the paddle. Press **R** to restart after a miss.

### How it works

Game state (ball position/direction, paddle position, brick mask, tick counter) is packed into query parameters each frame. A single-line render of the playfield is written into the URL path using `history.replaceState`, producing a Tiny Mario–style animation completely inside the address bar.
