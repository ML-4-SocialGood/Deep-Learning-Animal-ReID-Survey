---
layout: splash
title: "ReWildID Pro"
permalink: /tool/
header:
  overlay_filter: 0.1
  overlay_color: "#44308dff"
  caption: "AI-Powered Wildlife Re-Identification Platform for Conservation."
excerpt: "An open-source toolkit designed to identify species and re-identify individual animals using advanced machine learning."
actions:
  - label: "GitHub Repo"
    url: "https://github.com/ML-4-SocialGood/ReWildID"
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
  .badge-container img {
    margin-right: 5px;
    margin-bottom: 5px;
  }
</style>

<div style="text-align: center; max-width: 900px; margin: 0 auto;">
  <h2>From Research to Real-World Conservation</h2>
  
  <p style="font-size: 1.1em; color: #555; text-align: left; line-height: 1.6;">
    New Zealand is home to some of the world’s most unique fauna, but these native species face significant threats from invasive pests. One such predator is the stoat, which preys on the young of native birds. 
    Our client recognised this issue and tasked us with developing a platform to assist in monitoring and controlling the presence of stoats. The platform leverages machine learning and artificial intelligence to accurately identify stoats and other animals captured in photos. By utilising advanced image recognition algorithms, the platform can differentiate between various species, ensuring precise identification and effective monitoring. This innovative approach not only enhances the efficiency of pest control efforts but also contributes to the broader goal of preserving New Zealand’s unique biodiversity.
  </p>

  <div style="margin-top: 30px;">
    <a href="https://github.com/ML-4-SocialGood/ReWildID" class="btn btn--primary btn--large" style="text-decoration: none;">
      <i class="fab fa-github" style="margin-right: 8px;"></i> View Project on GitHub
    </a>
    <p style="font-size: 0.9em; margin-top: 10px; color: #888;">
      https://github.com/ML-4-SocialGood/ReWildID
    </p>
  </div>
</div>

---

## ✨ Key Features

<div class="feature-grid">
  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-mouse-pointer"></i></div>
    <h3>Ultra-Simple Workflow</h3>
    <p>Designed for efficiency. Simply <strong>drag & drop</strong> your camera-trap images, select "Re-ID", and let the AI handle the rest. The streamlined interface requires no coding knowledge to operate.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-search-location"></i></div>
    <h3>Detection & Classification</h3>
    <p>Automatically detect and classify wildlife using advanced <strong>YOLO and transformer models</strong>. The system filters empty frames and identifies species before processing individuals.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-fingerprint"></i></div>
    <h3>Individual Re-ID</h3>
    <p>Go beyond species level. ReWildID uses <strong>embedding-based recognition</strong> to match individual animals across different sightings, creating a timeline of unique identities.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-bolt"></i></div>
    <h3>Fast & Resilient</h3>
    <p>Built with a smart embedding cache and <strong>fault recovery</strong>. Re-run analyses in seconds, not minutes, and resume interrupted jobs seamlessly without losing data.</p>
  </div>

  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-images"></i></div>
    <h3>Media Library & Dashboard</h3>
    <p>Organize thousands of images with a powerful <strong>Gallery View</strong>. Visualize tracking data and get real-time insights via the built-in <strong>Analytics Dashboard</strong>.</p>
  </div>
  
  <div class="feature-card">
    <div class="feature-icon"><i class="fas fa-laptop-code"></i></div>
    <h3>Modern Tech Stack</h3>
    <p>A robust desktop application built on <strong>Electron, React, and TypeScript</strong>, powered by a local <strong>Python/PyTorch</strong> backend to ensure data privacy and offline capability.</p>
  </div>
</div>

---

## 🛠️ How It Works

ReWildID Pro integrates the CARE framework into a user-friendly GUI with three primary views:

1.  **Image Gallery View (Pre-processing):** Users upload raw camera-trap data via the Image Uploader. Images are automatically organized by date, ready for inspection and selection.
2.  **Animal Detection View:** Selected images are sent to the customized species detector. The system bounds and classifies animals, filtering out irrelevant data.
3.  **Animal ReID View:** The core phase. The toolkit employs the hosted model to extract embeddings and group individual animals with pseudo-identities. Results are sorted by date and time in the Data Directory Panel for easy review.