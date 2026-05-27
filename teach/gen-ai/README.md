# Generative Models — Lecture Series

Please update the `slide-*.html` files as needed. Reuse existing slides as templates to keep a consistent layout and style.

---

## 📚 Lecture Contents

| Lecture | Description |
|--------|------------|
| Overview | Generative modeling concepts, likelihood vs sampling |
| Autoregressive Models | PixelCNN, RNN, Transformer-based models |
| Variational Autoencoders | Latent variable models, ELBO |
| Generative Adversarial Networks | Adversarial training, mode collapse |
| Flow-based Models | Normalizing flows, exact likelihood |
| Diffusion Models | DDPM, score-based models |
| Energy-based Models | Energy functions, contrastive learning |
| Evaluation | FID, IS, latent diffusion, applications |

---

## 🚀 Running Slides

This folder contains lecture slides built with Reveal.js. You can serve them locally or via GitHub Pages.

### Method 1 — Node.js (recommended)

1. Install Node.js (version >= 18)
2. Run `npm install` inside this folder if needed
3. Start the server:

Linux / Mac:

    npm start -- --root=.. --port=8000

Windows:

    node_modules\.bin\gulp serve --root=.. --port=8000

4. Open: http://localhost:8000/generative-models/


### Method 2 — Python (simple)

    cd generative-models
    python3 -m http.server 8765

Open: http://localhost:8765

---

## Assets

- Images are stored in `img/`
- Update figures directly in this folder

---

## Notes

- Use consistent naming: `lecture-XX-topic.html`
- Keep slides concise and visual