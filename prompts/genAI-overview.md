# Prompt Template for Generating Reveal.js Slide Body Content

**ROLE**: You are a lecturer and Reveal.js slide designer. Convert provided lecture content into Reveal.js slide BODY content while matching the provided reference Reveal.js HTML deck’s structure, nesting, and styling patterns as closely as possible. Do not invent a new style system.

---

**INPUTS**:
### 1. Reference Reveal.js HTML file  
This is the canonical source of style and structure.

### 2. Lecture content  
This will be provided inside the CONTENT SECTION below. It may be empty in the template, but in actual use it will contain the source content for the lecture.

### 3. Optional metadata  
If provided, use it. Otherwise infer from the content and reference deck.
   - Course title (cover H1): <<...>>  
   - Lecture title (cover H3): <<...>>  
   - Lecture code/number: <<...>>  
   - Institution line (cover P): <<...>>  
   - Image folder prefix: <<...>>  
   - Preferred number of major parts: <<...>>  

---

**CONTENT**:

=== BEGIN CONTENT ===  

# Generative Models Overiview

# Part 1: Introduction to Generative Models (30 minutes)

## 1.1 What are Generative Models?
- Definition:
  - Models that learn the underlying distribution of data \( p(x) \)
  - Can generate new samples similar to training data
- Contrast with discriminative models:
  - Discriminative: learn \( p(y|x) \)
  - Generative: learn \( p(x) \) or \( p(x, y) \)

## 1.2 Why Generative Models Matter
- Applications:
  - Image generation (faces, art, medical images)
  - Text generation (LLMs)
  - Speech synthesis
  - Data augmentation
  - Simulation and scientific discovery
- Role in modern AI systems:
  - Foundation models
  - Multimodal learning

## 1.3 Types of Generative Tasks
- Unconditional generation
- Conditional generation
- Representation learning (latent space)
- Density estimation

## 1.4 Core Challenges
- High-dimensional distributions
- Mode collapse
- Training instability
- Evaluation difficulty

---

# Part 2: Probabilistic Foundations (30 minutes)

## 2.1 Probability Review
- Random variables, distributions
- Joint, marginal, conditional probability
- Expectation and likelihood

## 2.2 Maximum Likelihood Estimation (MLE)
- Objective:
  - Maximize \( \log p_\theta(x) \)
- Intuition:
  - Fit model to observed data
- Limitations:
  - Intractable likelihood for complex models

## 2.3 Latent Variable Models
- Introduce hidden variables \( z \)
- Model:
  - \( p(x) = \int p(x|z)p(z)dz \)
- Benefits:
  - Structured representation
  - Dimensionality reduction

## 2.4 Variational Inference
- Approximate posterior \( q(z|x) \)
- Evidence Lower Bound (ELBO):
  - Trade-off between reconstruction and regularization
- Key idea:
  - Turn inference into optimization

---

# Part 3: Classical Generative Models (45 minutes)

## 3.1 Gaussian Mixture Models (GMM)
- Mixture of Gaussians
- Expectation-Maximization (EM) algorithm
- Strengths:
  - Simple, interpretable
- Limitations:
  - Poor scalability for complex data

## 3.2 Autoregressive Models
- Factorization:
  - \( p(x) = \prod p(x_i | x_{<i}) \)
- Examples:
  - PixelRNN, PixelCNN
- Pros:
  - Exact likelihood
- Cons:
  - Slow sampling

## 3.3 Energy-Based Models (EBM)
- Define energy function instead of probability
- Sampling via MCMC
- Challenges:
  - Training difficulty
  - Sampling inefficiency

## 3.4 Flow-Based Models
- Invertible transformations
- Exact likelihood computation
- Examples:
  - RealNVP, Glow
- Trade-offs:
  - Memory cost
  - Architectural constraints

---

# Part 4: Deep Generative Models (50 minutes)

## 4.1 Variational Autoencoders (VAE)
- Architecture:
  - Encoder: \( q(z|x) \)
  - Decoder: \( p(x|z) \)
- Loss:
  - Reconstruction + KL divergence
- Strengths:
  - Stable training
  - Latent space structure
- Weakness:
  - Blurry outputs

## 4.2 Generative Adversarial Networks (GAN)
- Two-player game:
  - Generator vs Discriminator
- Objective:
  - Minimax optimization
- Variants:
  - DCGAN, WGAN, StyleGAN
- Issues:
  - Mode collapse
  - Training instability

## 4.3 Diffusion Models
- Forward process:
  - Add noise gradually
- Reverse process:
  - Learn to denoise
- Advantages:
  - High-quality samples
  - Stable training
- Cost:
  - Slow inference

## 4.4 Flow Matching & Modern Trends
- Learn continuous transformations
- Bridge between diffusion and flow models
- Key ideas:
  - Optimal transport
  - Straight-line flows
- Relevance:
  - Efficient generative modeling

---

# Part 5: Evaluation, Applications, and System Perspective (25 minutes)

## 5.1 Evaluation Metrics
- Likelihood-based:
  - Log-likelihood
- Sample quality:
  - FID (Fréchet Inception Distance)
  - IS (Inception Score)
- Diversity:
  - Mode coverage
- Human evaluation

## 5.2 Practical Considerations
- Compute requirements
- Training data scale
- Memory and GPU usage
- Inference latency

## 5.3 Applications Across Domains
- Computer vision:
  - Image synthesis, super-resolution
- NLP:
  - Text generation, translation
- Healthcare:
  - Medical image generation
- Robotics:
  - Simulation and planning

## 5.4 System-Level View (Important for AI Engineering)
- Workload characteristics:
  - Generative vs predictive
  - Latency vs offline
  - Stateless vs stateful
- Deployment challenges:
  - Serving large models
  - Scaling inference
  - Monitoring quality

## 5.5 Open Problems & Research Directions
- Controllability
- Interpretability
- Efficiency (faster sampling)
- Data efficiency
- Alignment and safety

=== END CONTENT ===  

Rules:
- This is the ONLY source of truth  
- Do NOT add external knowledge  
- Preserve meaning and structure  

---

**REQUIREMENTS**

### 1. Core Objective
- Preserve meaning and structure  
- Explain in concise, teachable English  
- Match reference structure and styling  


### 2. Output format
- Output ONLY `<section>` blocks  
- No `<html>`, `<head>`, `<body>`  
- No explanation  


### 3. Deck skeleton

#### Cover + Agenda wrapper
First output MUST be one top-level `<section>` with TWO slides:

- Cover:
  - `<h1>` course  
  - `<h3>` lecture  
  - `<p>` institution  

- Agenda:
  - `<h2>Content</h2>`  
  - `<ol>` major parts  



#### Major parts
- Create one top-level `<section>` per part  

First slide of each part MUST be:

```html
<section>
  <h1>
    <span class="text-light">K.</span><br />
    Section Name
  </h1>
</section>
```

Where `K = 1,2,3,...`


### 4. Slide patterns
- `<h2>` titles  
- `question-box` for definitions  
- `fragment` for reveal  
- `data-auto-animate` when needed  

Code blocks:

```html
<pre><code class="language-xxx" data-trim>...</code></pre>
```
Final slide with title: **Summary**  

### 5. Images / figures
- Suggest image by inserting the placeholder (do NOT invent filenames):
  <div class="placeholder" style="border:1px dashed #999;padding:18px;border-radius:8px;">
    <em>[Figure placeholder]</em><br/>
    <strong>Description:</strong> what the figure shows<br/>
    <strong>Image prompt:</strong> suggestion describing what image should be added here
  </div>

### 6. Content rules
- ONLY use CONTENT SECTION  
- NO hallucination  
- Keep logical flow  
- Allow:
  - split slides  
  - slight merge  


### 7. Writing style
- English only  
- 2–6 bullets per slide  
- Lecturer tone  

Highlight:
- `<span class="keyword">...</span>`
- `<span class="inline-code">...</span>`


### 8. Style reuse
- Use ONLY reference classes  
- Do NOT invent new components  

---

**OUTPUT**

Return ONLY:

- `<section>` blocks  
- no explanation  
- no extra text  

Return ONLY the `<section>` HTML blocks (the entire deck body) inside a Markdown ```html``` code block. No commentary outside HTML.