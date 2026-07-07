# Master — UET — Slide Decks

Coursework and thesis defence slides for the **Master's program in Information Technology** at University of Engineering and Technology (UET), Vietnam National University, Hanoi.

🌐 **Live:** [https://huynhspm.github.io/slides/study/master/](https://huynhspm.github.io/slides/study/master/)

---

## 📚 Slide Decks

| Course | Title | Materials | Status |
|--------|-------|-----------|--------|
| Statistical Machine Learning | Learning Conditional Generative Models for Phase Retrieval | [Paper](https://www.jmlr.org/papers/volume24/22-0106/22-0106.pdf) · [Slide](statistical-ml.html) | 🔜 Empty deck |
| Advanced Artificial Intelligence | High-Resolution Image Synthesis with Latent Diffusion Models | [Paper](https://arxiv.org/pdf/2112.10752) · [PDF](assets/pdf/latent-diffusion.pdf) · [Slide](advanced-ai.html) | 🔜 Empty deck |
| Thesis | Interpretable Prediction from 3D MRI Brain Scans in Multiple Sclerosis via Latent Representation Learning with Variational Autoencoders | [Paper](https://arxiv.org/pdf/2510.00051) · [Slide](thesis.html) | ✅ Available |
| Graduation Ceremony | Graduation Invitation | [Invitation](graduation-invitation.html) | ✅ Available |

`statistical-ml.html` and `advanced-ai.html` are currently placeholder decks (cover + footer only) — the paper-review content has not been written yet.

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
├── index.html                    # Topic index page (light/dark theme toggle)
├── index-style.css               # Index page styles
├── slide-style.css               # Shared Reveal.js slide styles
├── statistical-ml.html           # Statistical ML paper review (placeholder)
├── advanced-ai.html              # Advanced AI paper review (placeholder)
├── thesis.html                   # Thesis defence slides
├── graduation-invitation.html    # Graduation ceremony invitation
├── package.json
├── gulpfile.js
├── assets/
│   ├── img/
│   │   ├── uet.png               # UET logo
│   │   ├── background.avif
│   │   └── thesis/                # Thesis-specific figures
│   └── pdf/
│       └── latent-diffusion.pdf   # Advanced AI reference paper
├── plugin/                       # Reveal.js plugins (highlight, markdown, math/KaTeX, notes, search, zoom)
└── revealjs/                      # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server
