# Master — UET — Slide Decks

Coursework and thesis defence slides for the **Master's program in Computer Science** at University of Engineering and Technology (UET), Vietnam National University, Hanoi.

🌐 **Live:** [https://huynhspm.github.io/slides/study/master/](https://huynhspm.github.io/slides/study/master/)

---

## 📚 Slide Decks

| Course | Paper / Title | Status |
|--------|---------------|--------|
| [Statistical Machine Learning](statistical-ml.html) | [Learning Conditional Generative Models for Phase Retrieval](https://www.jmlr.org/papers/volume24/22-0106/22-0106.pdf) | ✅ Available |
| [Advanced Artificial Intelligence](advanced-ai.html) | [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/pdf/2112.10752) | ✅ Available |
| [Thesis](thesis.html) | [Interpretable Prediction from 3D MRI Brain Scans in Multiple Sclerosis via Latent Representation Learning with Variational Autoencoders](https://arxiv.org/pdf/2510.00051) | ✅ Available |

---

## 🚀 Running Slides

### Option 1 — Node.js (recommended)

```bash
cd study/master
npm install
npm start
```

Then open the URL shown in the terminal (typically `http://localhost:3000`).

### Option 2 — Static viewing

Open any `.html` file directly in your browser.

---

## 📁 Structure

```
study/master/
├── index.html              # Topic index page
├── index-style.css         # Index page styles
├── slide-style.css         # Shared slide styles
├── statistical-ml.html     # Statistical ML course slides
├── advanced-ai.html        # Advanced AI course slides
├── thesis.html             # Thesis defence slides
├── package.json
├── gulpfile.js
├── img/                    # Images and figures
│   └── thesis/             # Thesis-specific images
├── plugin/                 # Reveal.js plugins
└── revealjs/               # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server