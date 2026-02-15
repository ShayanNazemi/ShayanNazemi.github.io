---
layout: default
title: Home
---

<div class="hero two-col">

  <div class="hero-left">
    <img src="/assets/profile.jpg" alt="Shayan Nazemi" class="profile-pic">
  </div>

  <div class="hero-right">
    <h1>Shayan Nazemi</h1>

    <div class="actions">
      <a href="/assets/cv.pdf" target="_blank" rel="noopener">
        <i data-lucide="file-text"></i>
        Resume
      </a>

      <a href="https://github.com/ShayanNazemi" target="_blank" rel="noopener">
        <i data-lucide="github"></i>
        GitHub
      </a>

      <a href="mailto:nazemi.shayan@gmail.com">
        <i data-lucide="mail"></i>
        Email
      </a>

      <a href="https://www.linkedin.com/in/shayan-nazemi/" target="_blank" rel="noopener">
        <i data-lucide="linkedin"></i>
        LinkedIn
      </a>
    </div>
    <p>
      I am a PhD candidate in Data Science at HEC Montréal (Decision Sciences), 
      specializing in statistical modeling and machine learning for complex, 
      high-dimensional systems.
    </p>

    <p>
      My research focuses on Bayesian inference and hierarchical modeling, 
      with particular emphasis on skewed and heavy-tailed distributions in 
      spatio-temporal settings. I am particularly interested in market 
      microstructure, high-frequency trading, execution modeling, and 
      financial pricing.
    </p>
  </div>

</div>


<hr />

## Focus

- Depth-aware execution & order placement
- Slippage / fee modeling, fill probability
- Risk controls (inventory, limits, kill-switches)
- Backtesting & replay pipelines

## Featured projects

<div class="grid">
{% assign featured = site.projects | where: "featured", true | sort: "order" %}
{% for p in featured %}
  <div class="card">
    <h3><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
    <p>{{ p.summary }}</p>
    <div>
      {% for tag in p.tags %}
        <span class="pill">{{ tag }}</span>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>

<hr />

## Publications

<div class="pub-list">

  <div class="pub">
    <div class="pub-top">
      <div>
        <h3 class="pub-title">A Bayesian Framework for Post-disruption Travel Time Prediction in Metro Networks</h3>
        <p class="pub-authors">
          Shayan Nazemi, Aurélie Labbe, Stefan Steiner, Martin Trépanier, Léo R. Belzile
        </p>
        <p class="pub-venue">Manuscript in preparation</p>
      </div>

      <div class="badge" title="Status">
        <span class="badge-dot"></span>
        In preparation
      </div>
    </div>

    <div class="pub-meta">
      <span class="chip">Bayesian Statistics</span>
      <span class="chip">Spatiotemporal Statistics</span>
      <span class="chip">Metro Systems</span>
      <span class="chip">Transportation Networks</span>
    </div>

    <!-- Optional: add links when you have them -->
    <!--
    <div class="pub-links" style="margin-top:12px;">
      <a href="#" target="_blank" rel="noopener">PDF</a>
      <a href="#" target="_blank" rel="noopener">arXiv</a>
      <a href="#" target="_blank" rel="noopener">Code (private)</a>
    </div>
    -->
  </div>

</div>


## Notes on confidentiality

Core implementation is private (not open source).  
I’m happy to walk through design decisions, research methodology, and results, and share selected excerpts in an interview / under NDA.
