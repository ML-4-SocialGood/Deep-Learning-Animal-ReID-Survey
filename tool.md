---
layout: splash
title: "VIGIL-ReID Toolkit"
permalink: /tool/
header:
  overlay_filter: 0.1
  overlay_color: "#44308dff"
  caption: "Standardized Evaluation Toolkit for Animal Re-Identification (Animal ReID)."
excerpt: "A lightweight, modular, and extensible toolkit operationalizing the evaluation principles of our survey."
actions:
  - label: "GitHub Repo"
    url: "https://github.com/Jim-lyz1024/VIGIL-ReID"
classes: wide
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin: 40px 0;
  }
  .feature-card {
    background: #f8f9fa;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 25px;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.05);
  }
  .feature-icon {
    font-size: 2em;
    color: #44308d;
    margin-bottom: 15px;
  }
  h3 { margin-top: 0; }
  .code-block {
    background: #2d2d2d;
    color: #f8f8f2;
    padding: 20px;
    border-radius: 8px;
    font-family: monospace;
    overflow-x: auto;
  }
</style>

<div style="text-align: center; max-width: 900px; margin: 0 auto;">
  <h2>Standardizing Animal ReID Evaluation</h2>
  <p style="font-size: 1.1em; color: #555;">
    <strong>VIGIL-ReID</strong> (<strong>VI</strong>sion-<strong>L</strong>anguage <strong>G</strong>eneralizable <strong>I</strong>ntelligence <strong>L</strong>ibrary-ReID) is a standardized evaluation toolkit designed to support reproducible research.
  </p>
  <p>
    It operationalizes the benchmarking principles discussed in our survey, providing a unified framework for assessing methods under consistent, transparent protocols. 
    Rather than proposing new architectures, it focuses on <strong style="color:#44308d;">fair comparison</strong>, <strong style="color:#44308d;">result replication</strong>, and <strong style="color:#44308d;">systematic analysis</strong>.
  </p>
</div>

---

## 🚀 Key Capabilities

<div class="feature-grid">
  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-ruler-combined"></i></div>
    <h3>Standardized Metrics</h3>
    <p>Provides unified implementations of common retrieval metrics (CMC, mAP) specifically calibrated for Animal ReID tasks, ensuring numbers are comparable across different papers.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-project-diagram"></i></div>
    <h3>Structure-Aware Analysis</h3>
    <p>Goes beyond single numbers. Enables <strong>structure-aware benchmarking</strong> to interpret performance nuances across varying dataset scales, species complexities, and open-world settings.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-puzzle-piece"></i></div>
    <h3>Modular & Extensible</h3>
    <p>Designed with a plug-and-play architecture. Researchers can easily integrate <strong>new models</strong>, <strong>datasets</strong>, or custom <strong>evaluation protocols</strong> with minimal code changes.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-feather-alt"></i></div>
    <h3>Lightweight Integration</h3>
    <p>Non-intrusive design allows the toolkit to be incorporated into existing training pipelines as a standalone evaluation module.</p>
  </div>
</div>

---

## 📦 Installation & Usage

Ready to benchmark?

```bash
# Clone the repository
git clone [https://github.com/Jim-lyz1024/VIGIL-ReID.git](https://github.com/Jim-lyz1024/VIGIL-ReID.git)
cd VIGIL-ReID

# Install dependencies
pip install -r requirements.txt
```