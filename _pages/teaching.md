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

{% assign d = site.data.teaching %}
{% if d.princeton %}
  {% assign princeton = d.princeton %}
{% elsif d.teaching and d.teaching.princeton %}
  {% assign princeton = d.teaching.princeton %}
{% else %}
  {% assign princeton = nil %}
{% endif %}

{% if princeton %}
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
{% else %}
  <div class="teach-meta">No courses found.</div>
{% endif %}

<hr>

## The University of Texas at Austin
<div class="teach-meta"><em>Role: Teaching Assistant</em></div>

{% assign d = site.data.teaching %}
{% if d.ut_austin %}
  {% assign utaustin = d.ut_austin %}
{% elsif d.teaching and d.teaching.ut_austin %}
  {% assign utaustin = d.teaching.ut_austin %}
{% else %}
  {% assign utaustin = nil %}
{% endif %}

{% if utaustin %}
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
{% else %}
  <div class="teach-meta">No courses found.</div>
{% endif %}
