---
layout: default
title: Projects
permalink: /projects/
---

# Projects

<div class="grid">
{% assign ps = site.projects | sort: "order" %}
{% for p in ps %}
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
