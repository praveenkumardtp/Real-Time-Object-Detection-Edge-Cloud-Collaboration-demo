# Real-Time Object Detection — Edge–Cloud Collaboration (Demo)

**Short description (≤350 chars):**  
A browser-based demo that runs TensorFlow.js (coco-ssd) to perform real-time object detection on webcam video. Built as a lightweight front-end prototype to illustrate edge-device inference and visual feedback; runs fully in the browser (model files loaded from CDN) and needs only a local server or VS Code Live Server.

## Demo
This project demonstrates real-time object detection using TensorFlow.js and the `coco-ssd` model. Bounding boxes and labels are drawn over live webcam video in the browser. It’s intended as a front-end demo to showcase edge-side inference and visualization for an edge–cloud collaboration research prototype.

## Features
- Real-time object detection from webcam (no backend required)
- Animated bounding boxes and confidence labels
- FPS counter and simple start/stop controls
- Lightweight — model loaded from CDN (internet required)

## Files
- `index.html` — main demo page (HTML + JS)
- `styles.css` — styles and simple animations
- `README.md` — this file
- `README.txt` — quick-run notes
- `LICENSE` — license (MIT)

## How to run (recommended)
### Option A — VS Code Live Server (easiest for Windows)
1. Open the project folder in **VS Code**.
2. Install the **Live Server** extension by Ritwick Dey (if not already).
3. Right-click `index.html` → **Open with Live Server**.
4. Allow camera permission when the browser prompts.
> Live Server serves files over `http://localhost:PORT` so `getUserMedia()` works.

### Option B — Python simple HTTP server (if Python installed)
1. Open a terminal in the project folder.
2. Run (Python 3):  
   `python -m http.server 8000`  
3. Open `http://localhost:8000` in your browser.

If `python` is not found on Windows, you can:
- Install Python from https://www.python.org/ (check "Add to PATH" during install), or
- Use VS Code Live Server (Option A), or
- Use Node.js `http-server` (see below).

### Option C — Node (http-server)
1. Install Node.js (if needed).
2. In project folder run: `npx http-server -p 8000`
3. Open `http://localhost:8000`.

## Notes & troubleshooting
- The demo loads the TensorFlow.js model from CDN — an internet connection is required to fetch the model the first time.
- Camera access works on `http://localhost` or on HTTPS pages; `file://` (opening the HTML file directly) usually fails due to browser security.
- If camera permission is blocked, check browser site permissions and try again.
- Performance depends on CPU/GPU and browser; lower resolutions improve FPS.

## How to publish to GitHub Pages
1. Create a new GitHub repository and push this project.
2. In repo settings → Pages, select `main` branch and `/ (root)` folder as the source.
3. Save — your site will be available at `https://<username>.github.io/<repo-name>/`.
> Note: model CDNs must be accessible (internet) for the live site to work.

## Attribution
- Uses `@tensorflow/tfjs` and `@tensorflow-models/coco-ssd` from CDN.

---

## LICENSE (MIT)





Live demo: https://praveenkumardtp.github.io/Real-Time-Object-Detection-Edge-Cloud-Collaboration-demo/
