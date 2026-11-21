# Electric Ink - Computational Arts Workshop

The Computational Arts Workshop is a gateway to generative design, where logic meets expression. Dive into creative coding with p5.js v2 to build interactive graphics, breathing typography, physics systems like digital wind, and vector exports for physical pen plotter prints. No prior coding experience required.

## Quick Start: Web Editor Links

The easiest way to follow along with this workshop is directly in your browser. Click the links below to open the starter code/final code for each module in the official p5.js Web Editor:

*   **Module 1:** The Generative Mondrian — `[Link]`
*   **Module 2:** Responsive Brush — `[Link]`
*   **Module 3:** Kinetic Typography — `[Link]`
*   **Module 4:** Plotter Landscape (SVG Export) — `[Link]`

---

## Curriculum Outline

This repository contains local copies of all workshop materials. Each module includes a fully commented `sketch.js` file and a mini `README.md` with lesson notes.

### [Module 1: The Canvas and the Brush](./module-1-mondrian/)
Translating physical intuition onto a digital grid.
*   **Concepts:** The infinite loop (`setup` / `draw`), the coordinate system, geometric primitives, and state-machine styling.
*   **Project:** A generative, geometric abstraction inspired by Mondrian.

### [Module 2: Variables, Motion, and Interaction](./module-2-responsive-brush/)
Code becomes computational art when it breathes.
*   **Concepts:** Variables, system inputs (`mouseX`, `mouseY`), linear interpolation (`lerp`), and using math to map visual properties.
*   **Project:** A responsive digital brush where speed dictates thickness and position dictates color.

### [Module 3: Generative Typography](./module-3-generative-type/)
Treating typography as a collection of living particles.
*   **Concepts:** Deconstructing fonts with `textToPoints()`, arrays, and basic physics (gravity, springs, collision).
*   **Project:** A kinetic physics text that reacts to digital wind and tactile disruption.

### [Module 4: Bridging Digital and Physical](./module-4-plotter-export/)
Preparing generative art for pen plotters and laser cutters.
*   **Concepts:** Vector paths vs. raster pixels, nested loops, Perlin noise (`noise()`), and native SVG exporting in p5.js v2.
*   **Project:** A procedural topographic landscape exported as a mathematically perfect SVG.

---

## Local Development

If you prefer to run these sketches on your local machine rather than the p5.js Web Editor:

1. Clone this repository: `git clone https://github.com/lexotalin/electric-ink.git`
2. Open the folder in a code editor like VS Code.
3. Use an extension like **Live Server** to launch the `index.html` file of the module you want to run. *(Note: Module 3 requires to load the font asset).*

## Resources

*   [p5.js Quick Reference Guide](./p5js-quick-reference.md)
*   [Official p5.js Reference](https://p5js.org/reference/)

---

## License

This repository is dual-licensed to support both code reuse and curriculum protection:

*   **Code Examples & Scripts:** Licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute the code snippets for your own personal or commercial projects.
*   **Curriculum, & Text:** Licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](LICENSE-DOCS.md). You may share and adapt the written educational materials for non-commercial purposes, provided you give appropriate credit.
