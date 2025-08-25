---
layout: page
title:
permalink: /research/
nav: true
nav_order: 2

_styles: >
  .paper-block { margin-bottom: 1.5rem; }
  .paper-title { font-weight: 600; }
  .paper-meta  { color: #6c757d; }
  details.abstract {
    display: inline-block; margin-left: .5rem;
  }
  details.abstract summary {
    list-style: none; cursor: pointer; display: inline-block;
    padding: .25rem .5rem; border: 1px solid var(--global-theme-color, #6c757d);
    border-radius: .25rem; color: var(--global-theme-color, #6c757d);
    background-color: transparent; font-size: .875rem;
  }
  details.abstract[open] summary { background-color: rgba(0,0,0,.03); }
---

## Working Papers

{% assign working_papers = site.data.research.working_papers %}
<p style="color:#888">Count: {{ working_papers | size }}</p>

{% for p in working_papers %}
<div class="paper-block">
  <div class="paper-title">{{ p.title }}</div>
  {% if p.authors %}<div class="paper-meta">{{ p.authors }}</div>{% endif %}
  <div class="mt-1">
    {% comment %}
    {% if p.pdf %}
      <a class="btn btn-sm btn-outline-primary" href="{{ p.pdf | relative_url }}" target="_blank" rel="noopener">PDF</a>
    {% endif %}
    {% endcomment %}

    <details class="abstract">
      <summary>Abstract</summary>
      <div class="mt-2">{{ p.abstract | markdownify }}</div>
    </details>
  </div>
</div>
{% endfor %}

<hr>

## Work in Progress

{% assign wip_papers = site.data.research.work_in_progress %}
<p style="color:#888">Count: {{ wip_papers | size }}</p>

{% for p in wip_papers %}
<div class="paper-block">
  <div class="paper-title">{{ p.title }}</div>
  {% if p.authors %}<div class="paper-meta">{{ p.authors }}</div>{% endif %}
  <div class="mt-1">
    {% comment %}
    {% if p.pdf %}
      <a class="btn btn-sm btn-outline-primary" href="{{ p.pdf | relative_url }}" target="_blank" rel="noopener">PDF</a>
    {% endif %}
    {% endcomment %}

    {% comment %}
    <details class="abstract">
      <summary>Abstract</summary>
      <div class="mt-2">{{ p.abstract | markdownify }}</div>
    </details>
    {% endcomment %}
  </div>
</div>
{% endfor %}


