---
layout: default
title: Home
---

<div class="hero two-col">

  <div class="hero-left">
    <img src="{{ '/assets/profile.jpg' | relative_url }}" alt="Shayan Nazemi" class="profile-pic">
  </div>

  <div class="hero-right">
    <h1>Shayan Nazemi</h1>

    <div class="actions">
      <a href="{{ '/assets/cv.pdf' | relative_url }}" target="_blank" rel="noopener">
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
<p style="margin-top:10px;">
  <a href="{{ '/projects/' | relative_url }}">View all projects</a>
</p>

<hr />
## Featured publications

<div class="pub-list">
{% assign featured_pubs = site.publications | where: "featured", true | sort: "feature_order" %}
{% for p in featured_pubs %}
  <div class="pub">
    <div class="pub-top">
      <div>
        <h3 class="pub-title">
          <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
        </h3>
        {% if p.authors %}<p class="pub-authors">{{ p.authors }}</p>{% endif %}
        {% if p.venue %}<p class="pub-venue">{{ p.venue }}</p>{% endif %}
      </div>

      {% if p.status %}
        <div class="badge"><span class="badge-dot"></span>{{ p.status }}</div>
      {% endif %}
    </div>

    {% if p.tags %}
      <div class="pub-meta">
        {% for tag in p.tags %}
          <span class="chip">{{ tag }}</span>
        {% endfor %}
      </div>
    {% endif %}
  </div>
{% endfor %}
</div>

<p style="margin-top:10px;">
  <a href="{{ '/publications/' | relative_url }}">View all publications</a>
</p>


## Notes on confidentiality

Core implementation is private (not open source).  
I’m happy to walk through design decisions, research methodology, and results, and share selected excerpts in an interview / under NDA.
