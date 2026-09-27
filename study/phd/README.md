# PhD — VUB — Slide Decks

Coursework, progress-report and thesis slides for the **PhD programme** at Vrije Universiteit Brussel (VUB), Artificial Intelligence-supported Modelling in Clinical Sciences (AIMS).

🌐 **Live:** [https://huynhspm.github.io/slides/study/phd/](https://huynhspm.github.io/slides/study/phd/)

**Status:** 🟢 Ongoing (09/2026 – present)

---

## 📚 Slide Decks

| Course | Title | Materials | Status |
|--------|-------|-----------|--------|
| — | No slide decks yet | — | 🔜 Coming soon |

To add a deck: create `<deck-name>.html` (copy the Reveal.js boilerplate from `../master/statistical-ml.html`), then add a row to the table in `index.html` and here.

---

## 🚀 Running Slides

### Option 1 — Node.js (recommended)

```bash
cd study/phd
npm install
npm start
```

Then open the URL shown in the terminal (typically `http://localhost:3000`).

### Option 2 — Static viewing

Open any `.html` file directly in your browser.

---

## 📁 Structure

```
study/phd/
├── index.html                    # Topic index page (light/dark theme toggle)
├── index-style.css               # Index page styles
├── slide-style.css               # Shared Reveal.js slide styles
├── package.json
├── gulpfile.js
├── assets/
│   ├── img/
│   │   └── vub.png               # VUB logo
│   └── pdf/                      # Reference papers / exported PDFs
├── plugin/                       # Reveal.js plugins (highlight, markdown, math/KaTeX, notes, search, zoom)
└── revealjs/                     # Reveal.js library
```

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Plugins** — Highlight, Markdown, Math (KaTeX), Notes, Search, Zoom
- **Gulp** — local development server
