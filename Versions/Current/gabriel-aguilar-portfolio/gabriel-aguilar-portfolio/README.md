# Gabriel Aguilar — Portfolio

A minimal, editorial portfolio website for Gabriel Aguilar. Built as a single, self-contained HTML file with zero external dependencies. Open it in any browser and it works immediately.

---

## Live Demo

Once uploaded to GitHub, enable **GitHub Pages** (Settings → Pages → Deploy from branch → `main` / `root`) and your site will be live at:

```
https://yourusername.github.io/gabriel-aguilar-portfolio/
```

---

## Project Structure

```
gabriel-aguilar-portfolio/
│
├── index.html          ← The entire website (HTML + CSS + JS in one file)
│
├── assets/
│   └── pdfs/           ← Drop your résumé PDFs here
│       ├── gabriel-aguilar-film.pdf
│       ├── gabriel-aguilar-theater.pdf
│       └── gabriel-aguilar-creative-tech.pdf
│
├── README.md           ← This file
├── .gitignore          ← Tells Git what to ignore
└── CUSTOMIZE.md        ← Step-by-step guide to editing your content
```

---

## Pages

| Page | Description |
|------|-------------|
| **Home** | Bio, contact info, and photo |
| **Work** | Three interactive word clusters (Film, Theater, Creative Technology) with hoverable skill details |
| **Portfolio** | Tiled project grid with hover-reveal info panels and image lightbox |

---

## Quick Start

1. Clone or download this repository
2. Open `index.html` in any modern browser
3. Everything works immediately — no build step, no server required

---

## How to Customize

See **CUSTOMIZE.md** for a full walkthrough. The short version:

- **Bio / contact** — Edit the text directly in `index.html` around line 390
- **Skills and résumés** — Find `ALL_CLUSTERS` in the JavaScript section
- **Portfolio projects** — Find `ALL_PROJECTS` in the JavaScript section
- **Photo** — Replace the `<div class="home-photo-box">` with an `<img>` tag
- **PDFs** — Drop files into `assets/pdfs/` and update the `resumeFile` paths in `ALL_CLUSTERS`

---

## Technologies

- Pure HTML, CSS, and JavaScript
- Zero frameworks, zero dependencies
- Generative canvas animation (Bézier curves)
- SVG word cluster visualization
- CSS transitions for all animations

---

## Browser Support

Works in all modern browsers: Chrome, Firefox, Safari, Edge.

---

*Built with intentional restraint.*
