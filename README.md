# KREYNTIX MOTION STUDIO

Interactive Generative Cinema and Kinetic Motion Canvas Web Experience.

Live Deployment: [https://bryankwandou.github.io/kreyntix-motion-studio/](https://bryankwandou.github.io/kreyntix-motion-studio/)

## Overview

Kreyntix Motion Studio is an interactive motion landing page engineered to bridge generative AI video synthesis with modern high-performance web runtime standards. Inspired by progressive digital motion studios, the project demonstrates continuous frame-by-frame canvas scrubbing, multi-stream kinetic video feeds, and an interactive cinema showcase.

## System Architecture

```
kreyntix-motion-studio/
├── frames/                 # 240 losslessly extracted WebP sequence frames (Hero Canvas)
├── videos/                 # 20 optimized H.264 video clips + WebP thumbnail posters
├── videos.json             # Structured catalog metadata (titles, domains, specs)
├── index.html              # Semantic HTML5 layout, HUD telemetry, and cinema modal
├── styles.css              # Cyber-obsidian design system, typography scale, responsive grid
├── app.js                  # Canvas2D lerp engine, RAF loop, Web Audio synthesizer
└── README.md               # Technical documentation
```

## Technical Features

### 1. Scroll-Driven Canvas Frame Interpolation
- Hero sequence utilizes 240 high-resolution WebP frames extracted via FFmpeg from source motion video.
- Rendered on a responsive HTML5 Canvas with devicePixelRatio calibration for Retina/High-DPI displays.
- Linear interpolation (lerp) running within a 60 FPS requestAnimationFrame loop coordinates scroll distance with exact frame indices.
- Real-time telemetry overlay calculates speed (0-348 km/h), engine revs (1,100-8,400 RPM), and dynamic transmission gear states.
- Interactive manual scrubber and keyframe jump anchors (01 Aerodynamics, 02 Powertrain, 03 Cockpit POV) allow instant bi-directional navigation.

### 2. Kinetic Multi-Stream Video Reel
- Continuous dual-track horizontal marquee buffers presenting live generative clips in continuous loop.
- Lightweight web-optimized payloads (H.264 FastStart, 720p HD, sub-500KB per clip) for instantaneous playback without streaming stalls.

### 3. Curated Generative Cinema Showcase
- Catalog of 20 generative video productions across 4 technical domains:
  - Sci-Fi and Cybernetics
  - Atmospheric and Environment
  - Kinetic Dynamics
  - Character and Narrative
- Live category filtering, instant hover-play previews, and technical aspect ratio badges.

### 4. Theater Cinema Modal
- Fullscreen cinema player with playback speed controls (0.5x, 1.0x, 1.5x, 2.0x), scrub timeline, and keyboard shortcuts (Space to play/pause, Escape to exit).

### 5. Interactive Asset Inspector & Lab
- Diagnostic workbench enabling developers and visitors to inspect raster matrices, frame rate specs, container headers, and playback telemetry for any asset in the catalog.

### 6. Web Audio API Acoustic Engine
- Built-in audio synthesizer generating kinetic engine harmonics and frequency sweeps dynamically linked to canvas scroll velocity and RPM values without external audio assets.

## Local Execution

The project runs natively in any standard modern web browser without build tooling dependencies.

### Option 1: Direct File
Open `index.html` directly in Google Chrome, Microsoft Edge, Mozilla Firefox, or Safari.

### Option 2: Local HTTP Server
Using Python:
```bash
python -m http.server 8000
```
Then access `http://localhost:8000/`.

Using Node.js:
```bash
npx serve .
```

## Deployment

The application is deployed on GitHub Pages:
[https://bryankwandou.github.io/kreyntix-motion-studio/](https://bryankwandou.github.io/kreyntix-motion-studio/)
