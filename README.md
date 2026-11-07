# AI Growth Engine:  Interactive Pitch Platform & Vector PDF Synthesizer 🚀📊

<div align="center">

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![Framer Motion](https://img.shields.io/badge/Framer%20Motion-Animations-black?style=for-the-badge&logo=framer)](https://www.framer.com/motion/)
[![Client-Side PDF](https://img.shields.io/badge/jsPDF-Vector%20Export-red?style=for-the-badge)](https://github.com/parallax/jsPDF)

**A reactive, hardware-accelerated investor presentation engine featuring 14 animated slides, canvas particle physics, dynamic metric counters, and direct client-side vectorized PDF synthesis.**

[Architecture](#architecture--design) • [Slide Engine](#slide-deck-modules) • [PDF Synthesis](#client-side-pdf-synthesis) • [Getting Started](#quickstart)

</div>

---

## ⚡ Overview

Traditional investor pitch decks suffer from static presentation friction: PDFs are inert, web slide tools are sluggish, and exporting animated web content to a clean printable deck requires tedious manual duplication.

**AI Growth Engine** unifies web-native interactivity with offline artifact generation:
* **Interactive Presentation Mode:** 14 modular slides driven by Framer Motion transitions, particle canvas physics, and keyboard navigation.
* **Client-Side Vectorized PDF Synthesizer:** Direct compilation of live DOM components into publication-ready, multi-page vector PDF documents without server-side headless browsers (Puppeteer).
* **Live Financial & Metric Interpolation:** Animated counters rendering traction metrics with smooth requestAnimationFrame interpolation.

---

## 🏛️ Architecture & Design

```
┌────────────────────────────────────────────────────────────────────────┐
│                        AI GROWTH ENGINE PRESENTATION                   │
│                                                                        │
│   ┌─────────────────────┐   ┌─────────────────────┐   ┌────────────┐   │
│   │ Particle Background │   │  14 Modular Slides  │   │  Progress  │   │
│   │   (Canvas Physics)  │   │   (Framer Motion)   │   │  & Grid    │   │
│   └─────────────────────┘   └──────────┬──────────┘   └────────────┘   │
│                                        │                               │
│                   Keyboard Navigation  │  Export Trigger               │
│                   (Arrow Keys, Space)  │                               │
│                                        ▼                               │
│                     ┌────────────────────────────────────┐             │
│                     │ Client-Side PDF Synthesis Pipeline │             │
│                     │  (jsPDF + Vector Element Capture)  │             │
│                     └──────────────────┬─────────────────┘             │
└────────────────────────────────────────┼───────────────────────────────┘
                                         ▼
                        [Generated Multi-Page Deck.pdf]
```

---

## 🔬 Slide Deck Modules

The platform includes 14 structured slides covering the comprehensive startup lifecycle:
1. **Hero & Problem Formulation (`Slide1Hero.tsx` - `Slide3Problem.tsx`):** Executive positioning and market pain points.
2. **Solution & Architecture (`Slide4Solution.tsx` - `Slide7Tech.tsx`):** Technical moat and product walkthrough.
3. **Market Sizing & Business Model (`Slide8Market.tsx`, `Slide9Model.tsx`):** TAM/SAM/SOM calculation and unit economics.
4. **Competitive Moat & Traction (`Slide10Competition.tsx`, `Slide11Traction.tsx`):** Differentiation matrix and growth metrics.
5. **Capital Allocation & Roadmap (`Slide12Investment.tsx` - `Slide14CTA.tsx`):** Use of funds, milestone roadmap, and closing call-to-action.

---

## 📄 Client-Side PDF Synthesis (`generatePdf.ts`)

Instead of relying on heavy cloud rendering instances, the PDF pipeline executes entirely in-browser:
* Captures high-DPI slide canvas viewports with sub-pixel alignment.
* Compiles presentation themes into exact 16:9 aspect-ratio PDF pages using `jspdf`.
* Preserves color profiles, vector fonts, and layout bounds for presentation on projectors and mobile devices.

---

## 🛠️ Tech Stack Breakdown

- **Framework:** React 18, TypeScript, Vite
- **Animation & Physics:** Framer Motion (`framer-motion`), Canvas API
- **Document Export:** jsPDF (`jspdf`), html2canvas
- **UI & Layout:** Tailwind CSS, Radix UI Primitives, Lucide Icons

---

## 💻 Quickstart

```bash
# 1. Clone repository
git clone https://github.com/mdroushanalam-astra/ai-growth-engine.git
cd ai-growth-engine

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev
```

* **Keyboard Controls:** Use `Arrow Left` / `Arrow Right` to navigate slides, `F` for fullscreen, `G` for grid overview, and `D` or the export button to generate the PDF deck.

---

<div align="center">
  <sub>Engineered by <a href="https://github.com/mdroushanalam-astra">Md. Roushan Alam</a></sub>
</div>
