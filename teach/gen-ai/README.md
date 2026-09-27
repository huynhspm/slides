# Generative AI — Lecture Slides

Lecture slides for the **Generative AI** course, built with [Reveal.js](https://revealjs.com/).

This course provides a theoretical foundation in Generative AI, covering key generative modeling
paradigms from autoregressive models, VAEs, GANs, and normalizing flows to diffusion, latent
diffusion, DiT, and flow matching, with a primary focus on the principles and mathematical
foundations of modern image generation.

🌐 **Live:** [https://huynhspm.github.io/slides/teach/gen-ai/](https://huynhspm.github.io/slides/teach/gen-ai/)

---

## 📚 Lectures

### Part 1 — Foundations of Generative Modeling

| # | Lecture | Description |
|---|---------|-------------|
| 1 | [Introduction to Generative AI](lecture-01-introduction.html) | Modelling distributions, prediction vs generation, taxonomy and applications |
| 2 | [Probabilistic Foundations](lecture-02-probabilistic-foundations.html) | Distributions, chain rule, Bayes, entropy, KL divergence, MLE |
| 3 | [Latent Variable Models & Variational Inference](lecture-03-latent-variable-models.html) | GMM, EM, the intractable posterior, the ELBO |

### Part 2 — Likelihood-Based & Latent Generative Models

| # | Lecture | Description |
|---|---------|-------------|
| 4 | [Autoregressive Models I](lecture-04-autoregressive-1.html) | Chain-rule factorization, NADE, PixelRNN, PixelCNN, masked convolutions |
| 5 | [Autoregressive Models II](lecture-05-autoregressive-2.html) | Self-attention, causal masking, visual tokens, sampling strategies |
| 6 | [Variational Autoencoders](lecture-06-vae.html) | Encoder/decoder, the ELBO in practice, reparameterization trick |
| 7 | [Advanced VAEs](lecture-07-advanced-vae.html) | β-VAE, posterior collapse, VQ-VAE, VQGAN |
| 8 | [Normalizing Flows](lecture-08-normalizing-flows.html) | Change of variables, coupling layers, RealNVP, Glow |

### Part 3 — Implicit & Energy-Based Models

| # | Lecture | Description |
|---|---------|-------------|
| 9 | [Generative Adversarial Networks](lecture-09-gan.html) | Minimax game, optimal discriminator, JS divergence, DCGAN |
| 10 | [Advanced GANs & Image Translation](lecture-10-advanced-gan.html) | WGAN-GP, StyleGAN, pix2pix, CycleGAN |
| 11 | [Energy-Based Models & MCMC](lecture-11-energy-based-models.html) | Energy functions, contrastive divergence, Langevin dynamics |

### Part 4 — Diffusion, Score & Flow Matching

| # | Lecture | Description |
|---|---------|-------------|
| 12 | [Denoising Diffusion Models](lecture-12-diffusion-models.html) | Forward/reverse processes, noise schedules, the DDPM objective |
| 13 | [Score-Based Generation & Efficient Sampling](lecture-13-score-based-models.html) | Score matching, SDE/ODE view, DDIM, classifier-free guidance |
| 14 | [Latent & Conditional Diffusion](lecture-14-latent-diffusion.html) | Latent diffusion, U-Net, cross-attention, Stable Diffusion, ControlNet |
| 15 | [Flow Matching & Rectified Flow](lecture-15-flow-matching.html) | Conditional flow matching, optimal transport, straight trajectories |

### Part 5 — Visual GenAI: Evaluation, Scaling & Practice

| # | Lecture | Description |
|---|---------|-------------|
| 16 | [Evaluation of Generative Models](lecture-16-evaluation.html) | Likelihood, BPD, FID, precision/recall, CLIP score, human evaluation |
| 17 | [Large-Scale Visual Generation](lecture-17-multimodal-generation.html) | Web-scale data, CLIP, DiT, video/3D/audio overview |
| 18 | [Efficient, Safe & Deployable Visual GenAI](lecture-18-deployment-and-frontiers.html) | Distillation, consistency models, deployment, safety, open problems |

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

Open any `lecture-*.html` file directly in your browser.

---

## 📁 Structure

```
teach/gen-ai/
├── index.html              # Topic index page
├── index-page.css          # Index page styles
├── slide-style.css         # Shared slide styles
├── claude.md               # Slide-generation spec
├── lecture-01-introduction.html … lecture-18-deployment-and-frontiers.html
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
