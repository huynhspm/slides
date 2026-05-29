# 🎓 Slide Collection

Personal slide decks for **studying**, **researching**, and **teaching** — built with [Reveal.js](https://revealjs.com/) by **Trinh Ngoc Huynh**.

🌐 **Live site:** [https://huynhspm.github.io/slides/](https://huynhspm.github.io/slides/)

---

## 🗂 Repository Structure

```
.
├── index.html                  # Homepage — lists all decks by purpose
├── index-style.css             # Homepage styles
├── favicon.png
├── prompts/                    # Prompt templates (AI-assisted slide creation)
│   └── *.md
│
├── study/                      # 📚 Studying
│   ├── bachelor/               #    Bachelor — UET  ✅ 2 slide decks
│   │   ├── image-captioning.pdf
│   │   ├── thesis.pdf
│   │   ├── assets/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── master/                 #    Master — UET  ✅ 3 slide decks
│   │   ├── statistical-ml.html
│   │   ├── advanced-ai.html
│   │   ├── thesis.html
│   │   ├── img/
│   │   ├── plugin/
│   │   └── revealjs/
│   └── phd/                    #    PhD — VUB (coming soon)
│
├── research/                   # 🔍 Researching
│   ├── iai/                    #    IAI — UET  ✅ 3 presentations
│   ├── avitech/                #    AVITECH — UET  ✅ 1 presentation
│   └── aims/                   #    AIMS — VUB  ✅ 1 presentation
│
├── teach/                      # 👨‍🏫 Teaching
│   ├── ml/                     #    Machine Learning  ✅ 3 slide decks
│   │   ├── lecture-01-pca.html
│   │   ├── lecture-02-svd.html
│   │   ├── lecture-03-plsr.html
│   │   ├── img/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── gen-ai/                 #    Generative AI  ✅ 1 slide decks
│   │   ├── lecture-01-overview.html
│   │   ├── img/
│   │   ├── plugin/
│   │   └── revealjs/
│   ├── dl/                     #    Deep Learning  (planned)
│   └── cv/                     #    Computer Vision  (planned)
│
└── README.md
```

---

## 📚 Studying

| Track | Status | Content |
|-------|--------|---------|
| **Bachelor — UET** | ✅ Available | NLP (Image Captioning), Thesis |
| **Master — UET** | ✅ Available | Statistical ML, Advanced AI, Thesis |
| **PhD — VUB** | 🔜 Coming soon | Courses, Thesis |

---

## 🔍 Researching

| Lab | Supervisor | Topics |
|-----|------------|--------|
| **IAI — UET** | Dr. Tran Quoc Long | Generative Models, Diffusion Models, Flow Matching, Anomaly Detection, Uncertainty Segmentation, Lung Cancer Classification |
| **AVITECH — UET** | Prof. Dr. Nguyen Linh Trung | Seminars, Group Meetings, Paper Discussions |
| **AIMS — VUB** | Prof. Dr. Ir. Guy Nagels | Research Presentations, Latent Representation Learning, Brain Age Prediction, Biomarker Discovery |

---

## 👨‍🏫 Teaching

| Course | Status | Topics |
|--------|--------|--------|
| **Machine Learning** | ✅ Available | PCA, SVD, PLSR |
| **Generative AI** | ✅ Available | Overview & Likelihood vs Sampling, Autoregressive Models, VAE & GAN, Diffusion & Flow-based Models |
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
4. Add images/resources to `img/`
5. Update the root `index.html` to include the new topic card

---

## 👤 Author

**Trịnh Ngọc Huỳnh**

📧 [huynhtn@vnu.edu.vn](mailto:huynhtn@vnu.edu.vn) · [Huynh.Trinh.Ngoc@vub.be](mailto:Huynh.Trinh.Ngoc@vub.be)

🔗 [LinkedIn](https://www.linkedin.com/in/huynh-spm/) · 💻 [GitHub](https://github.com/huynhspm)