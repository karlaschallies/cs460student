# CS Final Project — 3D Animal Cell Study Guide (model-viewer) by Karla Schallies

## Main Goal
This project is a **3D interactive study guide** for an eukaryotic animal cell.  
The design choice is intentional: **labels use full explanatory text (not abbreviated captions)** to support deep learning and exam preparation. The goal is **conceptual mastery of structure–function relationships**, not entertainment.

---

## Project Overview
This site renders a 3D animal cell model in the browser using **Google’s `<model-viewer>`**. Students can:
- Rotate, zoom, and explore the cell in 3D
- Click organelle hotspots to **expand** and read detailed descriptions
- Collapse descriptions to keep the screen uncluttered

Hotspots are anchored to exact model locations using captured coordinates (`data-position` / `data-normal`) so labels remain attached while the model rotates.

---

## How to Use (For Students)
1. Open the website link (see “Live Demo” below).
2. Use your mouse/trackpad (or touch gestures) to rotate and zoom the model.
3. Click a hotspot to expand its description.
4. Click anywhere else to collapse.

---

## Live Demo
- GitHub Pages: https://karlaschallies.github.io/cs460student/

---

## How It Runs (Technical)
- The project is a static website (HTML/CSS/JS).
- The 3D model is loaded from a local `.glb` file:
  - `animal_cell.glb`
- Rendering + interaction is handled by `<model-viewer>`.

### Files (typical)
- `index.html` — main page, hotspots, and interaction logic
- `animal_cell.glb` — 3D model
- (optional in future) `animal_cell.usdz` — iOS AR Quick Look support

---

## Run Locally
Because browsers restrict loading local 3D assets from `file://`, you should run a local server.

### Option A: VS Code Live Server
1. Open the folder in VS Code
2. Install the **Live Server** extension
3. Right-click `index.html` → **Open with Live Server**

### Option B: Python (Terminal)
From the project folder:

```bash
python3 -m http.server 8000
