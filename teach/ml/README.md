# Machine Learning — Lecture Slides

Lecture slides for the **Machine Learning** course, built with [Reveal.js](https://revealjs.com/).

🌐 **Live:** [https://huynhspm.github.io/slides/teach/ml/](https://huynhspm.github.io/slides/teach/ml/)

---

## 📚 Lectures

| # | Course | Title | Materials | Status |
|---|--------|-------|-----------|--------|
| 1 | Dimensionality Reduction | Principal Component Analysis | [Slide](lecture-01-pca.html) | ✅ Available |
| 2 | Dimensionality Reduction | Singular Value Decomposition | [Slide](lecture-02-svd.html) | 🔜 Empty deck |
| 3 | Dimensionality Reduction | Partial Least Squares Regression | [Slide](lecture-03-plsr.html) | 🔜 Empty deck |

`lecture-02-svd.html` and `lecture-03-plsr.html` are currently placeholder decks (cover + footer only) — the lecture content has not been written yet.

---

## 🚀 Running Slides

### Option 1 — Node.js (recommended)

```bash
cd teach/ml
npm install
npm start
```

Then open the URL shown in the terminal (typically `http://localhost:3000`).

### Option 2 — Static viewing

Open any `lecture-XX-*.html` file directly in your browser.

---

## 📁 Structure

```
teach/ml/
├── index.html               # Topic index page (light/dark theme toggle)
├── index-style.css          # Index page styles
├── slide-style.css          # Shared Reveal.js slide styles
├── lecture-01-pca.html      # Principal Component Analysis
├── lecture-02-svd.html      # Singular Value Decomposition (placeholder)
├── lecture-03-plsr.html     # Partial Least Squares Regression (placeholder)
├── package.json
├── gulpfile.js
├── img/                     # Images and figures
│   └── lec-01/               # PCA lecture images
├── plugin/                  # Reveal.js plugins (highlight, markdown, math/KaTeX, notes, search, zoom)
└── revealjs/                 # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server
