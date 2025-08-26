---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 2
show_title: false
---

---
_styles: |
  /* Hide page H1 if the layout ignores `show_title: false` */
  .post-header .post-title { display: none; }

  .paper-block { margin-bottom: 1.5rem; }
  /* only the title text is bold, not the label */
  .paper-title { margin-bottom: .15rem; }
  .paper-title .title-text { font-weight: 600; }
  .paper-title .label { font-weight: 400; color: #6c757d; }
  .paper-meta  { color: #6c757d; }

  /* Abstract toggle styled as light-gray inline text with a leading > */
  details.abstract { display: inline-block; margin-left: .5rem; }
  details.abstract summary {
    list-style: none; cursor: pointer; display: inline; color: #999; font-size: .875rem;
  }
  details.abstract summary::-webkit-details-marker { display: none; }
  details.abstract summary::before { content: "> "; color: #999; }
  details.abstract[open] summary { background: transparent; }
---

## Working Papers

{% assign working_papers = site.data.research.working_papers %}
{% for p in working_papers %}
  {% assign co_size = p.coauthors | size %}
  <div class="paper-block">
    <div class="paper-title">
      <span class="title-text">{{ p.title }}</span>
      {% if p.label %} <span class="label">{{ p.label }}</span>{% endif %}
    </div>

    {% if co_size > 0 %}
      <div class="paper-meta">
        with
        {% for a in p.coauthors %}
          <a href="{{ a.url }}" target="_blank" rel="noopener">{{ a.name }}</a>{% unless forloop.last %}{% if forloop.index == co_size - 1 %} and {% else %}, {% endif %}{% endunless %}
        {% endfor %}
      </div>
    {% elsif p.authors %}
      <div class="paper-meta">{{ p.authors }}</div>
    {% endif %}

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
{% for p in wip_papers %}
  {% assign co_size = p.coauthors | size %}
  <div class="paper-block">
    <div class="paper-title">
      <span class="title-text">{{ p.title }}</span>
      {% if p.label %} <span class="label">{{ p.label }}</span>{% endif %}
    </div>

    {% if co_size > 0 %}
      <div class="paper-meta">
        with
        {% for a in p.coauthors %}
          <a href="{{ a.url }}" target="_blank" rel="noopener">{{ a.name }}</a>{% unless forloop.last %}{% if forloop.index == co_size - 1 %} and {% else %}, {% endif %}{% endunless %}
        {% endfor %}
      </div>
    {% elsif p.authors %}
      <div class="paper-meta">{{ p.authors }}</div>
    {% endif %}

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


