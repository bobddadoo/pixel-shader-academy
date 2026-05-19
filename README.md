# Pixel Shader Academy

> Learn GLSL the way you learn a video game.

[**🎮 Play the Free Demo →**](https://shader.dolstep.com) &nbsp;·&nbsp; [**🛒 Buy on itch.io →**](https://bobddadoo.itch.io/pixel-shader-academy-full-source) &nbsp;·&nbsp; [🌐 Landing site](https://bobddadoo.github.io/pixel-shader-academy/)

[한국어 안내](./README.ko.md)

![Pixel Shader Academy](./assets/banner.png)

---

## What is this?

**Pixel Shader Academy** is a browser-based, stage-by-stage GLSL fragment shader playground.
Write code on the right, watch the preview on top, read the lesson on the left, hit **Run** (or `Ctrl+Enter`), and let the **Check** button compare your output against the reference solution.

No install. No toolchain. No Node, no Unity, no headaches. Open a tab and start writing shaders.

> This repository is the **public landing page** for the project.
> The game itself is developed in a private repository and sold on itch.io.

---

## Why play it?

- **A real curriculum, not a pile of demos.** Every stage has authored lesson pages (EN + 한국어) that explain the concept, the GLSL builtins involved, and a hint-driven challenge.
- **Auto-grading at the press of a button.** The Check button renders your shader and the reference solution at multiple time samples and scores the per-channel difference. Tolerances are generous — no nitpicking over rounding errors.
- **Instant feedback.** CodeMirror 6 editor, Three.js fullscreen quad, `Ctrl+Enter` to compile. GLSL errors come back with named lines, not `ERROR: 0:42`.
- **Texture support.** Upload an image, crop it square with the built-in cropper, and sample it via `u_texture` from stage 6 onward.
- **Light and dark themes.** Cool-gray light palette for daylight, deep-purple dark mode for late-night shader hacking.

---

## What's inside (so far)

12 stages live today, with the curriculum growing toward 100 across 9 categories:

| # | Title | Concept |
|---|---|---|
| 1 | UV Gradient | `gl_FragCoord` → uv |
| 2 | Time-Based Blink | `u_time`, `mod`, `step` |
| 3 | Remap Sin to 0..1 | affine remap |
| 4 | Circle Mask | distance fields |
| 5 | Circle Outline | `smoothstep` for AA |
| 6 | Sample a Texture | `texture2D`, `u_texture` |
| 7 | Dissolve Effect | hash noise + threshold |
| 8 | Hit Flash | channel-isolated effects |
| 9 | Pixelation | `floor(uv * N) / N` |
| 10 | Wave Distortion | UV vs output distortion |
| 11 | Combine Everything | composition strategies |
| 12 | Cosine-Palette Kaleidoscope | IQ-style palettes + fract iteration |

More on the way — synthwave city, fire shaders, raymarched scenes, sprite atlases.

---

## Where to play

- **Free demo (always latest):** [shader.dolstep.com](https://shader.dolstep.com)
- **Full game on itch.io:** [bobddadoo.itch.io/pixel-shader-academy-full-source](https://bobddadoo.itch.io/pixel-shader-academy-full-source)

---

## Tech (for the curious)

- **Three.js** — fullscreen quad + `ShaderMaterial`, orthographic camera.
- **CodeMirror 6** — editor, theme injection, GLSL via `@codemirror/lang-cpp`.
- **Cropper.js** — texture cropping (square aspect).
- **Vite + TypeScript** — dev server, prod build.
- **No backend.** Everything runs in the browser; all state is `localStorage`.

---

## License & status

The **source code** for the game lives in a private repository and is sold as a commercial product on itch.io.
This repository contains the **public landing page** (`index.html`, banner art, README) and is MIT-licensed for that content.

---

## Credits

- Color palette technique on Stage 12: [Inigo Quilez's cosine palettes](https://iquilezles.org/articles/palettes/).
- Icon &amp; banner artwork: custom (graduation cap + shield + pixel gradient + chibi adventurers).
- Built with Claude Code (Anthropic).
