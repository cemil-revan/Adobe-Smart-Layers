# Adobe Stock — Smart Layers

A functional prototype of **Smart Layers**, a proposed feature for Adobe Stock that automatically decomposes a licensed stock image into independently editable layers — no manual masking required.

Built as a product design prototype to validate the core user experience before engineering investment.

**Live demo:** [cemil-revan.github.io/Adobe-Smart-Layers](https://cemil-revan.github.io/Adobe-Smart-Layers/)

**All code contained within index.html**

---

## What it does

Smart Layers addresses a core pain point in stock image workflows: users frequently find an image that is *almost* right but cannot change a single element without starting over. This prototype demonstrates the proposed solution.

**Decompose** — Click *Decompose Image* to trigger an AI-style decomposition sequence. The full image separates into five independently addressable layers: Background, Grapes, Banana, Pear, and Apple — each a 1080×1080 transparent PNG.

**Transform** — Select any layer from the Layers panel and drag it to reposition it on the canvas. Drag the corner handles to scale it up or down. Position and scale sync live to the Properties panel sliders.

**Color adjust** — Per-layer Hue, Brightness, and Saturation controls let you independently recolor any element without affecting the rest of the composition.

**Export** — Download the current canvas state as a full-resolution 1080×1080 PNG. Color adjustments are baked into the export via pixel-level processing, not CSS filters, ensuring accurate output across all browsers.

---

## Design reference

The interface mirrors the Adobe Stock asset detail page — dark theme, transparency checker canvas, metadata panel, and license selector — to simulate how Smart Layers would integrate into the existing product surface.

---

## Product context

This prototype was built to support a PRFAQ for Smart Layers and was informed by:

- User interviews identifying the core "close but not right" problem with flat stock image files
- Competitive analysis of Getty Images, Shutterstock, and Canva
- Evaluation criteria covering decomposition accuracy, layer integrity, and latency targets

The primary success metric is the **Smart Stock Download Rate (SSDR)** — the percentage of Smart Layers sessions resulting in at least one edited variant downloaded.

---

## Stack

Vanilla HTML, CSS, and JavaScript. No dependencies, no build step. Deployable directly via GitHub Pages.
