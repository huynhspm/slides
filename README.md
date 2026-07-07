# 🎓 Slide Collection

Personal slide decks for **studying**, **researching**, and **teaching** — built with [Reveal.js](https://revealjs.com/) by **Trịnh Ngọc Huỳnh**.

🌐 **Live site:** [https://huynhspm.github.io/slides/](https://huynhspm.github.io/slides/)

---

## 🗂 Repository Structure

```
.
├── index.html                  # Homepage — lists all decks by purpose, light/dark theme toggle
├── index-style.css             # Homepage styles
├── favicon.png
├── ai-agents.md                 # Behavioral guidelines for AI coding assistants
├── prompts/                     # Prompt templates (AI-assisted slide creation)
│   └── *.md
│
├── study/                       # 📚 Studying
│   ├── bachelor/                #    Bachelor — UET  ✅ available
│   │   ├── index.html
│   │   ├── assets/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── master/                  #    Master — UET  ✅ available
│   │   ├── index.html
│   │   ├── statistical-ml.html
│   │   ├── thesis.html
│   │   ├── graduation-invitation.html
│   │   ├── assets/
│   │   ├── plugin/
│   │   └── revealjs/
│   └── phd/                     #    PhD — VUB (coming soon, empty)
│
├── research/                    # 🔍 Researching
│   ├── iai/                     #    IAI — UET  ✅ available
│   ├── avitech/                 #    AVITECH — UET  ✅ available
│   └── aims/                    #    AIMS — VUB  ✅ available
│
├── teach/                        # 👨‍🏫 Teaching
│   ├── ml/                       #    Machine Learning  ✅ available
│   │   ├── index.html
│   │   ├── lecture-01-pca.html
│   │   ├── lecture-02-svd.html
│   │   ├── lecture-03-plsr.html
│   │   ├── img/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── gen-ai/                   #    Generative AI  ✅ available
│   │   ├── index.html
│   │   ├── lecture-01-overview.html
│   │   ├── img/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── dl/                       #    Deep Learning  (planned, empty)
│   └── cv/                       #    Computer Vision  (planned, empty)
│
└── README.md
```

Each topic folder (`study/*`, `research/*`, `teach/*`) is a self-contained Reveal.js project: its own `package.json`, `gulpfile.js`, bundled `revealjs/` core + `plugin/`, an `index.html` deck listing, and one `.html` file per lecture/presentation.

---

## 📚 Studying

| Track | Status | Content |
|-------|--------|---------|
| **Bachelor — UET** | ✅ Available | NLP, Thesis |
| **Master — UET** | ✅ Available | Statistical ML, Thesis, Graduation Invitation |
| **PhD — VUB** | 🔜 Coming soon | Courses, Thesis |

---

## 🔍 Researching

| Lab | Supervisor | Topics |
|-----|------------|--------|
| **IAI — UET** | Dr. Tran Quoc Long | AQF, MTMC, LDM |
| **AVITECH — UET** | Prof. Dr. Nguyen Linh Trung | Seminars |
| **AIMS — VUB** | Prof. Dr. Ir. Guy Nagels | Introduction |

---

## 👨‍🏫 Teaching

| Course | Status | Topics |
|--------|--------|--------|
| **Machine Learning** | ✅ Available | PCA, SVD, PLSR |
| **Generative AI** | ✅ Available | Overview & Likelihood vs Sampling |
| **Deep Learning** | 🔜 Planned | Neural Network Foundations, CNN, RNN / LSTM, Transformers & Attention |
| **Computer Vision** | 🔜 Planned | Image Classification, Object Detection, Semantic Segmentation, Vision-Language Models |

---

## 🚀 Usage

### Option 1 — Run locally (recommended)

Each slide deck has its own `package.json`. Navigate into a topic folder and start a local server:

```bash
cd teach/ml
npm install
npm run start
```

Then open the URL shown in the terminal (typically `http://localhost:3000`).

### Option 2 — Static viewing

Open any `.html` file directly in your browser.

---

## 🛠 Tech Stack

- **[Reveal.js](https://revealjs.com/)** — slide presentation framework
- **Reveal.js Plugins** — Highlight, Markdown, Math (KaTeX / MathJax), Notes, Search, Zoom
- **Gulp** — local development tasks per topic

---

## ➕ Adding New Content

1. Create a new folder under the appropriate directory (`study/`, `research/`, or `teach/`)
2. Copy an existing topic folder as a template (e.g. `teach/ml/`)
3. Update the topic's `index.html`
4. Add images/resources to `img/` (or `assets/`)
5. Update the root `index.html` to include the new topic card

---

## 👤 Author

**Trịnh Ngọc Huỳnh**

📧 [huynhtn@vnu.edu.vn](mailto:huynhtn@vnu.edu.vn) · [Huynh.Trinh.Ngoc@vub.be](mailto:Huynh.Trinh.Ngoc@vub.be)

🔗 [LinkedIn](https://www.linkedin.com/in/huynh-spm/) · 💻 [GitHub](https://github.com/huynhspm)
