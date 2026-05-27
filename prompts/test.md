# Prompt Template for Generating Reveal.js Thesis Defense Slides

## **ROLE**
You are a Master’s student and expert Reveal.js slide designer.
Your task is to convert thesis content into Reveal.js slide BODY content while closely matching the provided reference Reveal.js HTML deck in:
- Structure
- Section hierarchy
- Nesting style
- Class usage
- Animation patterns
- Layout conventions
- Typography patterns

Do NOT invent a new design system.
The reference deck is the canonical source of styling and presentation structure.

---

## **INPUTS**:
## 1. Reference Reveal.js HTML Deck
The provided Reveal.js HTML file defines:
- layout structure
- reusable classes
- animation style
- typography conventions
- visual hierarchy
- component usage

Reuse its style patterns as faithfully as possible.

## 2. Thesis Content
The thesis content will appear inside the CONTENT SECTION below. This content is the ONLY source of truth.

You MUST:
- preserve meaning
- preserve logical structure
- preserve technical correctness

You MUST NOT:
- add external knowledge
- hallucinate missing technical details
- invent experiments, figures, results, or citations

### 3. Optional metadata  
If provided, use it. Otherwise infer from the content and reference deck.
   - Thesis title (cover H1): <<INTERPRETABLE PREDICTION FROM 3D MRI BRAIN SCANS IN MULTIPLE SCLEROSIS VIA LATENT REPRESENTATION LEARNING WITH VARIATIONAL AUTOENCODERS>>  
   - Major: <<Computer Science>> and Code: <<8480101>>
   - Name: <<Trinh Ngoc Huynh>>
   - Supervisor: <<Dr. Tran Quoc Long>>
   - Co-Supervisor: <<Prof. Dr. Ir. Guy Nagels>>
   - Image folder prefix: <<img/thesis/>>
   - Preferred number of major parts: <<...>>  

---

## **CONTENT**:

=== BEGIN CONTENT ===  


1. Introduction
- Motivation
- Research Problem and Objectives

2. Related Work
2.1. Cognitive Impairment in Multiple Sclerosis
- Conventional Clinical Assessment
- Standardized Neuropsychological Assessment
- Neuroimaging Assessment
2.2. Neuroimaging Predictive Methods
- Machine Learning Methods
- Deep Learning Methods
- Latent Representation Learning Methods

3. Methodology
3.1 Latent Representation Learning for 3D Images
- Latent Representation Learning
- Mutual Information Regularization
3.2 Latent Representations for Interpretable Prediction
- Prediction from Latent Representations
- Latent Space Analysis

4. Experiments
- Datasets
- Results
  - Structural Information in Latent Representations
  - Latent Representation Informativeness
  - Interpretable Biomarker Prediction

5. Conclusion
- Main Findings
- Limitations
- Future Work

=== END CONTENT ===  

Rules:
- This section is the ONLY source of content
- Preserve terminology and technical meaning
- Keep logical thesis flow
- Do not fabricate missing information

---

## **REQUIREMENTS**

### 1. Core Objective
You MUST:
- preserve thesis meaning
- preserve logical structure
- present slides in professional academic English
- follow the reference Reveal.js deck structure and styling
- generate presentation-ready slides

### 2. Output format
- Output ONLY `<section>` blocks  
- No `<html>`, `<head>`, `<body>`  
- No explanation and markdown commentary

### 3. Deck skeleton

#### Cover + Agenda wrapper
The FIRST top-level <section> MUST contain TWO nested slides:
- Cover Slide:
  - `<h1>` thesis title
  - `<h2>` student name
  - `<h3>` major + major code
  - `<p>` institution/supervisors  

- Agenda: (nice format)
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

## **OUTPUT**

Return ONLY:

- `<section>` blocks  
- no explanation  
- no extra text  

Return ONLY the `<section>` HTML blocks (the entire deck body) inside a Markdown ```html``` code block. No commentary outside HTML.