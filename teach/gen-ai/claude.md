# Prompt: Generate Reveal.js Slide Content from Lecture Material

**ROLE**: You are a lecture designer and Reveal.js specialist. Transform lecture content into Reveal.js HTML slides using the provided reference deck as a style and structure template. Do not create new styling or invent content.

---

## INPUT SECTIONS

### 1. Reference Reveal.js Deck
- Use this as the canonical source for all HTML structure, CSS classes, and design patterns
- Match nesting, spacing, and component usage exactly

### 2. Lecture Content
Provided below in CONTENT SECTION. May be empty in template; will contain actual content in use.

### 3. Metadata (optional)
If not provided, infer from content:
  - Course Title (H1 on cover): Generative AI
  - Lecture Title (H3 on cover): Introduction to Generative AI
  - Lecture Number/Code: Lecture 1
  - Institution Name: Institute for Artificial Intelligence
  - Image Folder Path: "img/lec01"
  - Expected Major Sections: [number, e.g., 3–5]

---

## CONTENT SECTION

=== BEGIN CONTENT ===  

Introduction to Generative AI

1. What is Generative AI?
  Definition of Generative AI
  Generation vs prediction
  Examples: text, image, audio, video, 3D, code
  Generative AI vs traditional AI/ML
  Một vài modern examples để tạo motivation

2. Discriminative vs Generative
  Discriminative: p(y∣x)
  Generative: p(x) / p(x,y)
  Classification vs generation
  Intuition bằng image classification vs image generation
  Có thể introduce conditional generation: p(x∣c)

3. Learning & Sampling from Data Distributions
  Data distribution p_data(x)
  Model distribution p_θ(x)
  Learning the distribution
  Likelihood: does the model explain observed data?
  Sampling: can the model generate new data?
  Noise/latent variable → generated sample
  Preview các cách tiếp cận khác nhau:
  autoregressive
  latent variable
  GAN
  diffusion
  Không cần đi sâu KL/MLE/ELBO ở đây; chỉ tạo intuition để Lecture 02–03 formalize.

4. Why Is Generative Modeling Hard?
  High-dimensional data
  Complex / multimodal distributions
  Long-range dependencies
  Quality vs diversity
  Likelihood vs perceptual quality
  Sampling speed
  Compute and memory
  Evaluation difficulty

5. History, Taxonomy & Applications
- History of Generative Models
  Classical probabilistic models
  Autoregressive models
  Variational Autoencoders (VAEs)
  Generative Adversarial Networks (GANs)
  Normalizing Flows
  Diffusion Models
  Flow Matching & Rectified Flow
  Foundation & Multimodal Generative Models
- Taxonomy of Generative Models
  Autoregressive Models — factorize the data distribution into conditional probabilities
  Latent Variable Models — introduce latent representations to model complex data
  Normalizing Flows — learn invertible transformations with tractable likelihoods
  GANs — learn generation through adversarial training
  Energy-Based Models — model data through an energy function
  Diffusion Models — learn to reverse a gradual noising process
  Flow Matching — learn continuous transport dynamics from noise to data
- Applications
  Text & code generation
  Text-to-image & image generation
  Image editing & inpainting
  Video generation
  Audio & music generation
  3D generation
  Scientific & molecular generation
  Multimodal generation

=== END CONTENT ===  

**Rule**: Content between markers is the ONLY source of truth. Do NOT add external knowledge or assume details not present.

---

## REQUIREMENTS

### Output Format
- Return ONLY `<section>` blocks
- No `<html>`, `<head>`, `<body>`, or `<div class="reveal">`
- No explanatory text outside the code block
- Wrap output in a single Markdown `html` code fence

### Deck Structure

#### Slide 1: Cover Slide
````html
<section>
  <h1>[Course Title]</h1>
  <h3>[Lecture Title]</h3>
  <p>[Institution]</p>
</section>
````

#### Slide 2: Agenda
````html
<section>
  <h2>Content</h2>
  <ol>
    <li>Section 1 Name</li>
    <li>Section 2 Name</li>
    <li>Section 3 Name</li>
  </ol>
</section>
````

#### Major Sections (one `<section>` per section)
Each major section begins with a title slide:
````html
<section>
  <h1><span class="text-light">N.</span><br />Section Name</h1>
</section>
````
where `N = 1, 2, 3, ...`

Content slides within each section use `<h2>` for slide titles.

### Slide Content Patterns

| Element | HTML | Usage |
|---------|------|-------|
| Slide Title | `<h2>Title</h2>` | Primary heading on content slides |
| Bullet List | `<ul><li>...</li></ul>` | 2–6 items per slide |
| Definition/Key Concept | `<div class="question-box"><strong>Term:</strong> definition</div>` | Highlight important definitions |
| Reveal Animation | `<li class="fragment">Item</li>` | Progressive disclosure of bullets |
| Code Block | `<pre><code class="language-python" data-trim>...</code></pre>` | Inline or multi-line code (use appropriate language tag) |
| Keyword Highlight | `<span class="keyword">term</span>` | Emphasize key concepts |
| Inline Code | `<span class="inline-code">variable</span>` | Technical terms in text |

### Image / Figure Handling
When an image is needed, insert a placeholder:
````html
<div class="placeholder" style="border:1px dashed #999;padding:18px;border-radius:8px;">
  <em>[Figure X: Descriptive Title]</em><br/>
  <strong>Description:</strong> Brief explanation of what the figure shows<br/>
  <strong>Image prompt:</strong> Detailed visual description for generating or sourcing the image
</div>
````

### Summary Slide
Final slide of the deck (after all sections):
````html
<section>
  <h2>Summary</h2>
  <ul>
    <li>Key takeaway 1</li>
    <li>Key takeaway 2</li>
    <li>Key takeaway 3</li>
  </ul>
</section>
````
---

## Content Rules

1. **Single Source of Truth**: Use ONLY the content in the CONTENT SECTION
2. **No Hallucination**: Do not add external knowledge, examples, or context not in source
3. **Preserve Logic**: Maintain the original structure and flow of the lecture
4. **Flexibility**:
   - Split a topic across 2–3 slides if needed for clarity
   - Merge minor topics into one slide if they logically belong together
   - Adjust section boundaries only if content structure demands it

---

## Writing Style

- **Language**: English only
- **Tone**: Professional lecture tone, accessible to students
- **Slide Content**:
  - 2–6 bullet points per slide
  - Clear, concise sentences
  - Active voice preferred
- **Text Emphasis**:
  - Wrap keywords in `<span class="keyword">...</span>`
  - Wrap code/technical terms in `<span class="inline-code">...</span>`

---
## Styling Rules

- **Use ONLY reference classes**: `text-light`, `keyword`, `inline-code`, `question-box`, `placeholder`, `fragment`, `language-*`
- **Do NOT invent CSS classes or styling**
- **Do NOT add inline styles except for placeholders** (border, padding, border-radius as shown)
- Rely entirely on the reference deck's stylesheet

---

## FINAL OUTPUT

Return a single Markdown code block containing ONLY the complete `<section>` HTML for the entire deck:

````html
<section>
  ...
</section>

<section>
  ...
</section>

...
````

**No extra text, no explanations, no commentary outside the code block.**