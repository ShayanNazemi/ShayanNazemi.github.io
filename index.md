---
layout: default
title: Home
---

<div class="hero">
  <h1>Your Name</h1>
  <p>Quantitative Research • Market Microstructure • Systematic Trading</p>

  <div class="actions">
    <a href="/assets/Your_Name_Resume.pdf">Resume (PDF)</a>
    <a href="https://github.com/YOUR_USERNAME" target="_blank" rel="noopener">GitHub</a>
    <a href="mailto:you@email.com">Email</a>
    <a href="https://www.linkedin.com/in/YOUR_HANDLE" target="_blank" rel="noopener">LinkedIn</a>
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

## Notes on confidentiality

Core implementation is private (not open source).  
I’m happy to walk through design decisions, research methodology, and results, and share selected excerpts in an interview / under NDA.
