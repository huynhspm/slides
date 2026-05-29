# Machine Learning — Lecture Slides

Lecture slides for the **Machine Learning** course, built with [Reveal.js](https://revealjs.com/).

🌐 **Live:** [https://huynhspm.github.io/slides/teach/ml/](https://huynhspm.github.io/slides/teach/ml/)

---

## 📚 Lectures

| # | Lecture | Description | Status |
|---|---------|-------------|--------|
| 1 | [Principal Component Analysis](lecture-01-pca.html) | Dimensionality reduction, eigendecomposition, and data projection | ✅ Available |
| 2 | [Singular Value Decomposition](lecture-02-svd.html) | Matrix factorization, low-rank approximation, and applications | ✅ Available |
| 3 | [Partial Least Squares Regression](lecture-03-plsr.html) | Supervised dimensionality regression, covariance maximization | ✅ Available |

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
├── index.html              # Topic index page
├── index-style.css         # Index page styles
├── slide-style.css         # Shared slide styles
├── lecture-01-pca.html
├── lecture-02-svd.html
├── lecture-03-plsr.html
├── package.json
├── gulpfile.js
├── img/                    # Images and figures
│   └── lec-01/             # PCA lecture images
├── plugin/                 # Reveal.js plugins
└── revealjs/               # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server