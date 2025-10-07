*“My object detector spotted my coffee mug 47 times this morning. I think it’s trying to tell me something about caffeine dependence.”*

# Object Detection (Browser)

🔗 **Live demo:** https://ghoshsrinjoy.github.io/object-detect-demo/

A single-page, client-side object detection app. No server. No API keys. Just a webcam, some JavaScript, and models that try not to call your coffee mug a donut. Works great on GitHub Pages (HTTPS) and embeds cleanly in Google Sites. 📷

---

## Executive Summary

This project shows real-time, in-browser object detection with a simple model selector. Pick a model, allow camera access, and watch boxes + labels render on a canvas. Everything runs on the client, so sharing a link is all it takes. ⚡

**Why it’s useful**
- Instant demo for stakeholders or classes, no installs.
- Works on laptops and phones.
- Easy to fork, tweak, and host on any static site.

---

## Business Problem

Spinning up infra just to test detection is a pain. Teams need a zero-setup way to:
- Validate behavior on real video quickly.
- Share experiments via a link, no accounts, no tokens.
- Prototype education/kiosk experiences that must run fully in the browser.

This repo cuts the overhead to nearly zero. 🧪

---

## Methodology

**Flow**
1. Request webcam with `getUserMedia`.
2. Let the user choose a model from the dropdown.
3. Run inference per frame and draw boxes/labels on a canvas.
4. Drive the loop with `requestAnimationFrame` for smooth UX.

**Model selector**
- **COCO-SSD (TF.js, `lite_mobilenet_v2`)** : fast startup, 80 classes, good mobile performance.
- **YOLOv8n (Transformers.js)** : strong accuracy/speed trade-off, slightly larger download.
- **DETR-ResNet-50 (Transformers.js)** : robust in crowded scenes; heavier and slower.

**Features**
- Real-time drawing of bounding boxes and labels.
- Everything client-side; no network calls after model load.
- Clean UI with loading status and errors surfaced clearly. 🧭
**Quick start (local preview)**  

To try it locally, run a simple web server and open the app in your browser:  

## Using Python

python -m http.server 8080

Or using Node

npx http-server -p 8080

Then open http://localhost:8080 in your browser, allow camera access when prompted, and you’re ready to start detecting. 📷

## Skills

This project highlights: JavaScript (ES modules), HTML/CSS, TensorFlow.js & Transformers.js, MediaDevices `getUserMedia`, Canvas 2D, async loading, simple performance hygiene (throttling where needed), and friendly UX for ML demos (permissions, loading, failure states). 🛠️

---

## Results & Business Recommendation

**What you get**
- ⚡ **Zero backend** and **zero keys**
- 📷 **Live detection** directly in the browser
- 🔗 **Shareable link** that works on most modern devices

**Which model to default to**
- Start with **COCO-SSD** for instant load and wide compatibility.  
- Offer **YOLOv8n** as the balanced option for laptops/desktops.  
- Keep **DETR-ResNet-50** as the advanced choice for dense scenes or stronger machines.

---

## Recommendation

Ship with **COCO-SSD** selected. Prefetch **YOLOv8n** after idle so switching feels snappy. Label **DETR** as heavier but robust in busy scenes. That balance keeps first-time users happy while giving power users a clear upgrade path. 🎯

---

## Next Steps

🖼️ Add upload mode (images/videos) alongside webcam.  
📊 Show FPS/latency overlay to compare models.  
🧵 Move inference into a Web Worker for extra UI smoothness.  
🎬 Add snapshot/record options for sharing results.  
📦 Package as a PWA for offline kiosk use.  
♿ Improve accessibility: keyboard start/stop, clearer errors.  
🔧 Add confidence thresholds & per-class filters to tune predictions.

---

*Happy detecting!* 🤖


::contentReference[oaicite:0]{index=0}

