# Bachelor — UET — Slide Decks

Coursework and thesis slides for the **Bachelor's program in Information Technology** at University of Engineering and Technology (UET), Vietnam National University, Hanoi.

🌐 **Live:** [https://huynhspm.github.io/slides/study/bachelor/](https://huynhspm.github.io/slides/study/bachelor/)

---

## 📚 Slide Decks

| Course | Title | Materials |
|--------|-------|-----------|
| Natural Language Processing | Image Captioning | [PDF](assets/pdf/image-captioning.pdf) · [Slide](image-captioning.html) |
| Computer Graphics | Diffusion Model | [PDF](assets/pdf/diffusion-model.pdf) · [Slide](diffusion-model.html) |
| Thesis | Diffusion Model in Latent Space for Medical Image Segmentation | [PDF](assets/pdf/thesis.pdf) · [Slide](thesis.html) |

Each `.html` deck is a Reveal.js rebuild of the corresponding PDF, with math rendered via KaTeX and diagrams redrawn as HTML/CSS flow boxes.

---

## 📁 Structure

```
study/bachelor/
├── index.html               # Topic index page (light/dark theme toggle)
├── index-style.css          # Index page styles
├── package.json
├── gulpfile.js
├── image-captioning.html    # Reveal.js deck — NLP: Image Captioning
├── diffusion-model.html      # Reveal.js deck — Computer Graphics: Diffusion Model
├── thesis.html               # Reveal.js deck — Bachelor thesis
├── slide-style.css           # Shared Reveal.js slide styles (keyword, question-box, flow-diagram)
├── assets/
│   ├── img/
│   │   └── uet.png          # UET logo
│   └── pdf/                 # Original presentation PDFs
│       ├── image-captioning.pdf
│       ├── diffusion-model.pdf
│       └── thesis.pdf
├── plugin/                  # Reveal.js plugins (highlight, markdown, math/KaTeX, notes, search, zoom)
└── revealjs/                 # Reveal.js library
```
