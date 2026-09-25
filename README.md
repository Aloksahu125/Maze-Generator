# Maze Generator — Recursive Backtracking

A browser-based maze generator built with [p5.js](https://p5js.org/), visualizing the recursive backtracking algorithm in real time as it carves a perfect maze every time it loads out of a grid.

## How it works

- The canvas is divided into a grid of square cells, each starting with all four walls intact.
- Starting from the top-left cell, the algorithm repeatedly:
  1. Marks the current cell as visited and highlights it.
  2. Picks a random unvisited neighbor (if any exist).
  3. Removes the wall between the current cell and that neighbor.
  4. Pushes the current cell onto a stack and moves to the neighbor.
  5. If a cell has no unvisited neighbors, it backtracks by popping the last cell off the stack.
- This continues until every cell has been visited, producing a maze with exactly one path between any two points (no loops, no isolated regions).

The algorithm is implemented iteratively using an explicit stack rather than actual function recursion, but follows the same logic as the classic recursive backtracking approach.

## Tech

- **p5.js** for canvas rendering and the animation loop
- Vanilla JavaScript, HTML, CSS — no build step, no dependencies beyond the p5.js CDN

## Run locally

Clone the repo and open `index.html` in a browser — no server or build step required.

```bash
git clone https://github.com/Aloksahu125/Maze-Generator.git
cd maze-generator
open index.html
```

## File structure

```
├── index.html   # entry point, loads p5.js and sketch.js
├── style.css    # minimal full-window canvas styling
└── sketch.js    # grid setup, maze generation loop, Cell logic
```

---

**Short description (for GitHub's "About" field):**
> Browser-based maze generator visualizing the recursive backtracking algorithm in real time, built with p5.js.
