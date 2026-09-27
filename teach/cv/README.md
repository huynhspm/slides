# Generative AI — Lecture Slides

Lecture slides for the **Generative AI** course, built with [Reveal.js](https://revealjs.com/).

🌐 **Live:** [https://huynhspm.github.io/slides/teach/gen-ai/](https://huynhspm.github.io/slides/teach/gen-ai/)

---

## 📚 Lectures

| # | Lecture | Description | Status |
|---|---------|-------------|--------|
| 1 | [Overview](lecture-01-overview.html) | Introduction to generative modeling — likelihood vs sampling, major model families | ✅ Available |

### Planned

| # | Topic | Description |
|---|-------|-------------|
| 2 | Autoregressive Models | PixelCNN, RNN, Transformer-based models |
| 3 | Variational Autoencoders | Latent variable models, ELBO |
| 4 | Generative Adversarial Networks | Adversarial training, mode collapse |
| 5 | Flow-based Models | Normalizing flows, exact likelihood |
| 6 | Diffusion Models | DDPM, score-based models |
| 7 | Energy-based Models | Energy functions, contrastive learning |
| 8 | Evaluation | FID, IS, latent diffusion, applications |

---

## 🚀 Running Slides

### Option 1 — Node.js (recommended)

```bash
cd teach/gen-ai
npm install
npm start
```

Then open the URL shown in the terminal (typically `http://localhost:3000`).

### Option 2 — Static viewing

Open `lecture-01-overview.html` directly in your browser.

---

## 📁 Structure

```
teach/gen-ai/
├── index.html              # Topic index page
├── index-page.css          # Index page styles
├── slide-style.css         # Shared slide styles
├── lecture-01-overview.html
├── package.json
├── gulpfile.js
├── img/                    # Images and figures
├── plugin/                 # Reveal.js plugins
└── revealjs/               # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server