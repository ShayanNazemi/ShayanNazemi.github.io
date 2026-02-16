---
layout: default
title: Publications
permalink: /publications/
---

# Publications

<div class="pub-list">
{% assign pubs = site.publications | sort: "order" %}
{% for p in pubs %}
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
