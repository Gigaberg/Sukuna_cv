# 🩸 Malevolent Shrine – Gesture Controlled Domain Expansion

A real-time 3D recreation of Sukuna’s **“Malevolent Shrine”** built using Three.js and MediaPipe hand tracking.

Activate the domain through a live hand gesture and watch the shrine emerge with cinematic lighting, bloom effects, camera motion, and background audio — all running directly in the browser.

---

## 🎬 Inspiration

This project was inspired by the SAT0RU WebGL domain expansion project.  
While the original focused on Gojo’s techniques, this version reimagines the concept by recreating Sukuna’s “Malevolent Shrine” with custom gesture logic, cinematic animation, and enhanced visual effects.

---

## ✨ Features

- 🎥 Real-time webcam hand tracking (MediaPipe)
- ✋ Custom gesture activation (middle-finger domain trigger)
- 🔵 1.2s cursed energy charging animation
- 🏯 3D GLTF shrine model rendering
- 🌫 Cinematic fog and volumetric lighting
- ✨ Bloom post-processing effects
- 🎵 Sukuna background music activation
- 📸 Smooth camera lerp & shrine float animation
- ⚡ Dynamic light flicker and particle effects

---

## 🛠 Tech Stack

- **Three.js** – WebGL rendering & scene management
- **MediaPipe Hands** – Real-time gesture detection
- **GLTF Loader** – 3D shrine model
- **EffectComposer + UnrealBloomPass** – Post-processing effects
- **Web Audio API (Three.Audio)** – Background music

---

## 🚀 How It Works

1. The webcam feed is captured using MediaPipe.
2. Hand landmarks are analyzed per frame.
3. When the correct gesture (middle finger up) is detected:
   - A cursed energy charge begins.
   - After 1.2 seconds, the domain activates.
4. The shrine appears with cinematic lighting and audio.

---

## 🖥 Running Locally

Because the project uses ES modules and webcam access, it must run on a local server.

### Option 1: VS Code Live Server
1. Install the Live Server extension.
2. Right-click `index.html`.
3. Click **“Open with Live Server”**.

### Option 2: Simple Python Server
```bash
python -m http.server 8000
