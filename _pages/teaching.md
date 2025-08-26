---
layout: page
permalink: /teaching/
title: Teaching
nav: true
nav_order: 3
show_title: false

_styles: |
  /* Hide page H1 if show_title doesn't work in your layout */
  .post-header .post-title { display: none; }

  .teach-block { margin-bottom: 1rem; }
  .teach-title { font-weight: 600; }
  .teach-meta  { color: #6c757d; font-size: .95rem; }
---

## Princeton University
<div class="teach-meta"><em>Role: Teaching Assistant</em></div>

{% assign princeton = site.data.teaching.princeton %}
{% for t in princeton %}
<div class="teach-block">
  <div class="teach-title">{{ t.course }}</div>
  <div class="teach-meta">
    {{ t.level }}
    {% if t.instructor %} — with {{ t.instructor }}{% endif %}
    {% if t.term %} ({{ t.term }}){% endif %}
  </div>
</div>
{% endfor %}

<hr>

## The University of Texas at Austin
<div class="teach-meta"><em>Role: Teaching Assistant</em></div>

{% assign utaustin = site.data.teaching.ut_austin %}
{% for t in utaustin %}
<div class="teach-block">
  <div class="teach-title">{{ t.course }}</div>
  <div class="teach-meta">
    {{ t.level }}
    {% if t.instructor %} — with {{ t.instructor }}{% endif %}
    {% if t.term %} ({{ t.term }}){% endif %}
  </div>
</div>
{% endfor %}
