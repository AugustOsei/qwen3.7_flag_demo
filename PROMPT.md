# Interactive Flag Lab — AI Coding Prompt

Use this prompt with an AI coding assistant (Qwen Code, Claude, GPT-4, etc.) to build a similar WebGL cloth simulation project from scratch.

---

## 📋 Copy This Prompt

```
Build an interactive WebGL cloth simulation demo as a single self-contained HTML file. No external dependencies, no frameworks — pure vanilla JavaScript with custom GLSL shaders.

## Core Requirements

Create a real-time cloth physics simulation of a flag on a chrome pole with these features:

### Physics Engine
- Spring-mass cloth simulation using Verlet integration
- 38x24 particle grid with structural, shear, and bend constraints
- Iterative constraint solving (6-14 iterations based on stiffness)
- Configurable parameters: wind speed/direction, turbulence, gusts, stiffness, damping, gravity, bend resistance
- Mouse/touch interaction — drag the cloth directly

### Rendering (Custom GLSL Shaders)
- **Cloth shader**: Two-sided lighting with silk sheen, rim lighting, key light + fill light, specular highlights. Texture-based lighting that brightens branded elements on the fabric
- **Pole shader**: Brushed metallic silver finish with vertical streaks, specular highlights, rim lighting
- **Background shader**: Sky texture with cinematic vignette, color grading, subtle drift animation
- **Bloom post-processing**: Multi-pass — scene to FBO → brightness extraction → Gaussian blur (2 passes) → composite with film grain

### Visual Design
- Dark, cinematic aesthetic with glassmorphism UI panels
- Accent color: neon green (#39FF14)
- Background: dusk/night sky (use a placeholder gradient or sky image)
- Flag fabric: near-black with white branding (monogram, wordmark, geometric accents)
- Chrome pole with decorative finial ball

### Interactive Controls (Glassmorphism Panel)
- Sliders: Wind (0-30), Direction (-1 to 1), Turbulence (0-1), Gust (0-1), Stiffness (0.1-1), Damping (0.9-1), Gravity (0-1), Bend Resistance (0-1)
- Wind presets with smooth transitions: Calm Breeze, Coastal Flow, Storm Pulse, Showcase
- Buttons: Gust trigger, Reset, Debug wireframe, Quality toggle (Hi/Lo), Auto-orbit camera
- Flag style swatches (6 colors: Midnight, Wine, Navy, Forest, Charcoal, Racing checkered)

### Flag Texture Generation
- Procedurally generate flag textures on a 2D canvas at runtime
- Include branding: centered monogram in circle, wordmark, subtitle, accent lines, corner details
- Use system fonts (-apple-system, Helvetica Neue)
- Champagne gold or white branding on dark fabric

### Camera & Interaction
- Orbit camera with mouse drag (or touch)
- Auto-orbit toggle (starts after 2s idle)
- Smooth intro unfurl animation (3 seconds, ease-out)
- Mouse proximity wind effect (pushes cloth away from cursor)

### Bonus Features (Add These Last)

**Birds in Background:**
- 5 procedural birds with V-shaped silhouettes flying across the sky
- Wing flapping animation with varying speeds
- Rendered between sky and flag for depth

**Wind Audio (Web Audio API):**
- Procedural wind sound using brown and pink noise (no audio files)
- Four layers: main wind (bandpass), low rumble (lowpass), turbulence (pink noise bandpass), high whistle
- Volume and frequency respond to wind speed, turbulence, gust parameters in real-time
- Sound toggle button (off by default, browsers require user interaction)

**UI Polish:**
- Glassmorphism header panel with title and description
- Footer with link to your website
- Debug wireframe overlay showing cloth mesh

## Technical Constraints
- Single HTML file, everything inline (CSS, JS, GLSL shaders)
- No external libraries (no Three.js, no gl-matrix)
- Hand-write mat4/vec3 math utilities
- Responsive — full viewport canvas
- Mobile-friendly with touch support

## Build Incrementally
1. Start with basic cloth physics and rendering
2. Add interactive controls
3. Implement flag textures and branding
4. Add bloom post-processing
5. Polish camera and animations
6. Add birds and audio last

## Visual Reference
- Dark cinematic look with neon green accents
- Glassmorphism UI (blurred dark panels with subtle borders)
- Clean, premium aesthetic — no glow/bloom/emissive effects on branding
- Prioritize visual polish and smooth animations
```

---

## 🎯 Expected Output

After running this prompt, you should get a single HTML file with:

- ✅ Real-time cloth physics simulation
- ✅ Interactive wind controls with presets
- ✅ Multiple flag styles with procedural textures
- ✅ Custom GLSL shaders for cinematic rendering
- ✅ Bloom post-processing with film grain
- ✅ Chrome pole with metallic finish
- ✅ Sky background with vignette
- ✅ Drag interaction (mouse + touch)
- ✅ Auto-orbit camera option
- ✅ Debug wireframe mode
- ✅ Intro unfurl animation
- ✅ Birds flying in background
- ✅ Procedural wind audio (Web Audio API)
- ✅ Glassmorphism UI panels
- ✅ Zero external dependencies

---

## 💡 Tips for Best Results

1. **Build incrementally** — Don't ask for everything at once. Start with the core physics, then layer features.

2. **Reference this repo** — Tell the AI: "Look at the code in this repo for implementation details" and point to specific files.

3. **Be specific about visual style** — If you want a different color scheme (e.g., gold instead of white, different accent color), say so explicitly.

4. **Test frequently** — Ask the AI to open the HTML in your browser after each major feature.

5. **Iterate on details** — Say things like "make the cloth stiffer," "slow down the unfurl animation," or "reduce bloom intensity" to fine-tune.

6. **Performance tuning** — If it's slow, ask to reduce the cloth grid size (e.g., 24x16 instead of 38x24).

---

## 🔄 Customization Ideas

Once you have the base working, try these variations:

- **Your own branding** — Replace "AW" / "AUGUST WHEEL" with your logo
- **Different flag designs** — Country flags, company logos, abstract patterns
- **Particle effects** — Add rain, snow, or leaves blowing in the wind
- **Day/night cycle** — Animate the sky and lighting over time
- **Audio visualization** — Make the flag respond to music or microphone input
- **Multiple flags** — Add more poles with different flags
- **Fabric types** — Silk, cotton, metal mesh (different physics parameters)

---

## 📚 Learn More

- **Cloth simulation**: Verlet integration + constraint solving
- **WebGL basics**: [webglfundamentals.org](https://webglfundamentals.org)
- **GLSL shaders**: [thebookofshaders.com](https://thebookofshaders.com)
- **Web Audio API**: [developer.mozilla.org/docs/Web/API/Web_Audio_API](https://developer.mozilla.org/docs/Web/API/Web_Audio_API)

---

## 🤝 Share Your Version

If you build something cool with this prompt, share it! Tag it with **#InteractiveFlagLab** or **#WebGLCloth**.

Happy coding! 🚩
