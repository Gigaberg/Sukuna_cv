# 🩸 Malevolent Shrine – Gesture Controlled Domain Expansion

A real-time 3D recreation of Sukuna’s **Malevolent Shrine** built with Three.js + MediaPipe hand tracking.

Trigger techniques with live hand gestures and watch cinematic lighting, bloom, model animation, particles, and music unfold in the browser.

---

## ✨ Features

- 🎥 Real-time webcam hand tracking (MediaPipe Hands)
- ✋ Multi-gesture technique detection (Cleave, Dismantle, Shrine)
- 🔴 Domain expansion sequence with flash + overlay effects
- 🏯 GLTF shrine model loading and scene integration
- 🌫 Fog, layered lighting, red sky, and blood-ground atmosphere
- ✨ Post-processing with Unreal Bloom
- 🎵 Looping Sukuna background audio
- 📸 Smooth camera transition + continuous scene animation

---

## 🎮 Gestures & Controls

| Gesture | Detected Technique | Notes |
|---|---|---|
| Thumb + index pinch (`distance < 0.04`) | **Cleave** | Fast slash-like particle pattern |
| Index up + middle down | **Dismantle** | Distinct slicing pattern |
| Index + middle + ring + pinky up | **Domain Expansion: Malevolent Shrine** | Triggers shrine activation sequence |

> Gesture logic is implemented in `index.html` inside `hands.onResults(...)`.

---

## 🛠 Tech Stack

- **Three.js** – scene/rendering/camera/lights/audio
- **MediaPipe Hands** – real-time hand landmarks
- **GLTFLoader** – shrine model loading (`./models/shrine.glb`)
- **EffectComposer + UnrealBloomPass** – bloom post-processing
- **Three.Audio** – background music (`./assets/sukuna.mp3`)

---

## ✅ Prerequisites

- A modern browser with webcam support (Chrome/Edge recommended)
- Camera permission enabled
- Run from `localhost` (or HTTPS) — not plain `file://`
- Internet access (CDN imports are used for Three.js and MediaPipe)

---

## 🚀 Run Locally

Because this project uses ES modules and webcam APIs, run it on a local server.

### Option 1: VS Code Live Server

1. Install the **Live Server** extension.
2. Right-click `index.html`.
3. Choose **Open with Live Server**.

### Option 2: Python HTTP server

```bash
python -m http.server 8000
```

Then open:

- `http://localhost:8000`

When prompted, allow camera access.

---

## 📁 Project Structure

```text
.
├── index.html              # Main app (scene, gestures, effects, animation)
├── models/
│   └── shrine.glb          # Required shrine model
├── assets/
│   └── sukuna.mp3          # Background audio
└── README.md
```

---

## 🧪 Troubleshooting

- **Camera feed not showing**
  - Ensure browser camera permissions are enabled.
  - Verify you are running from `localhost`/HTTPS, not opening `index.html` directly.

- **No audio playback**
  - Some browsers block autoplay audio until user interaction.
  - Click/tap once on the page to allow audio.

- **Shrine not visible**
  - Confirm `models/shrine.glb` exists at the expected path.
  - Check browser console for model loading errors.

- **Blank/partial scene**
  - Confirm network access is available for CDN script/module imports.

---

## 🎬 Inspiration & Credit

Inspired by the SAT0RU WebGL domain expansion concept, reimagined here with Sukuna’s **Malevolent Shrine** aesthetic and custom gesture flow.
