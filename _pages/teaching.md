---
layout: page
permalink: /teaching/
title: Teaching
nav: true
nav_order: 3
show_title: false

_styles: >
  .teach-block { margin-bottom: 1rem; }
  .teach-title { font-weight: 600; }
  .teach-meta  { color: #6c757d; }
---

## Princeton University

{% assign princeton = 
  [
    {
      "course": "POL 396: International Organization",
      "level": "Undergraduate",
      "role":  "Teaching Assistant",
      "instructor": "Jim Vreeland",
      "term": "Spring 2024"
    },
    {
      "course": "POL 572: Quantitative Analysis I",
      "level": "Graduate",
      "role":  "Teaching Assistant",
      "instructor": "rocio Titiunik",
      "term": "Spring 2023"
    },
    {
      "course": "POL 573: Quantitative Analysis II",
      "level": "Graduate",
      "role":  "Teaching Assistant",
      "instructor": "Rocio Titiunik",
      "term": "Fall 2023"
    }
  ]
%}

{% for t in princeton %}
<div class="teach-block">
  <div class="teach-title">{{ t.course }}</div>
  <div class="teach-meta">
    {{ t.level }} — {{ t.role }}
    {% if t.instructor %} — with {{ t.instructor }}{% endif %}
    {% if t.term %} ({{ t.term }}){% endif %}
  </div>
</div>
{% endfor %}

<hr>

## The University of Texas at Austin

{% assign utaustin = 
  [
    {
      "course": "FIN 357: Business Finance",
      "level": "Undergraduate",
      "role":  "Teaching Assistant",
      "instructor": "Robert Duvic",
      "term": "2018–2020"
    },
    {
      "course": "STA 380: Mathematical Statistics for Applications",
      "level": "Graduate",
      "role":  "Teaching Assistant",
      "instructor": "Thomas Sager",
      "term": "Fall 2017"
    },
    {
      "course": "PHY 103M: Laboratory for Physics",
      "level": "Undergraduate",
      "role":  "Teaching Assistant",
      "instructor": "",
      "term": "Spring 2017"
    }
  ]
%}

{% for t in utaustin %}
<div class="teach-block">
  <div class="teach-title">{{ t.course }}</div>
  <div class="teach-meta">
    {{ t.level }} — {{ t.role }}
    {% if t.instructor != "" %} — with {{ t.instructor }}{% endif %}
    {% if t.term %} ({{ t.term }}){% endif %}
  </div>
</div>
{% endfor %}
