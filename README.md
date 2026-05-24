# August Wheel — Interactive Flag Lab

A real-time WebGL cloth simulation featuring interactive flag physics, dynamic wind, and cinematic rendering — built entirely with vanilla JavaScript and custom GLSL shaders.

![WebGL Cloth Simulation](https://img.shields.io/badge/WebGL-Cloth%20Simulation-39FF14?style=flat-square)
![Vanilla JS](https://img.shields.io/badge/Stack-Vanilla%20JS%20%2B%20WebGL-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)

## ✨ Features

- **Real-time cloth physics** — spring-mass simulation with structural, shear, and bend constraints
- **Interactive controls** — tune wind speed, direction, turbulence, gusts, stiffness, damping, gravity, and bend resistance
- **Drag the fabric** — grab and interact with the cloth directly
- **Wind presets** — Calm Breeze, Coastal Flow, Storm Pulse, and Showcase with smooth transitions
- **Multiple flag styles** — Midnight, Wine, Navy, Forest, Charcoal, and Racing (checkered)
- **Cinematic rendering** — custom GLSL shaders for silk sheen, rim lighting, two-sided illumination, bloom post-processing, and film grain
- **Chrome pole** — brushed metallic finish with decorative finial
- **Auto-orbit camera** — toggleable automatic camera rotation
- **Debug wireframe** — visualize the cloth mesh in real time
- **Intro unfurl animation** — smooth cloth deployment on load
- **Touch support** — works on mobile devices
- **Zero dependencies** — pure HTML/CSS/JS, no frameworks or libraries

## 🚀 Live Demo

**[View Live Demo](https://qwen3-7-flag-demo.vercel.app)** ← *update if Vercel assigns a different URL*

## 🛠️ Running Locally

No build step required. Open the file directly or serve with any static server:

```bash
# Option 1: Open directly
open index.html

# Option 2: Python server
python3 -m http.server 8000

# Option 3: Node server
npx serve .
```

Then visit `http://localhost:8000` (or the port shown).

## 📁 Project Structure

```
├── index.html          # Main application (self-contained)
├── flag-demo.html      # Same file (original name)
├── sky.png             # Sky background texture
├── .gitignore
├── LICENSE
└── README.md
```

## 🎨 Technical Highlights

- **Cloth simulation**: Verlet integration with iterative constraint solving
- **Rendering pipeline**: Multi-pass — scene → FBO → bloom extraction → Gaussian blur → composite
- **Lighting**: Key light + fill + rim + silk sheen, two-sided for cloth
- **Math**: Hand-written mat4/vec3 utilities (no gl-matrix dependency)
- **Textures**: Flag textures generated procedurally on a 2D canvas at runtime

## 🤖 Built With

This project was developed using **Qwen Code** (qwen3.7-max) as an AI coding assistant, demonstrating AI-assisted creative development.

## 📄 License

MIT — see [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

- Sky background texture generated with GPT Image 2.0
- Built with [Qwen Code](https://qwen.ai)
