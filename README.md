# Object Detection (Browser)

A single-page, **client-side** object detection demo hosted on **GitHub Pages** and embedded in **Google Sites**.  
No server, no API keys, everything runs in the user’s browser.

**Live URL**  
`https://ghoshsrinjoy.github.io/object-detect-demo/`

---

## Features

- Works with your **webcam** (HTTPS required — GitHub Pages is).
- **Model selector**:
  - **COCO-SSD (TF.js, lite_mobilenet_v2)** – fast startup, 80 classes, good mobile performance.
  - **YOLOv8n (Transformers.js)** – strong accuracy/speed trade-off, slightly larger download.
  - **DETR-ResNet-50 (Transformers.js)** – robust in crowded scenes; heavier and slower.
- Draws bounding boxes and labels in real time.

---

## Quick start (local preview)

Just open `index.html` in a browser. For the webcam to work locally, prefer a local web server:

```bash
# Python
python -m http.server 8080
# or Node
npx http-server -p 8080

