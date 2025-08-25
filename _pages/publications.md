---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 2
---

_styles: >
  details.abstract {
    display: inline-block;
    margin-left: .5rem;
  }
  details.abstract summary {
    list-style: none;
    cursor: pointer;
  }
  details.abstract summary::-webkit-details-marker { display: none; }
  details.abstract summary {
    display: inline-block;
    padding: .25rem .5rem;
    border: 1px solid var(--global-theme-color, #6c757d);
    border-radius: .25rem;
    color: var(--global-theme-color, #6c757d);
    background-color: transparent;
    font-size: .875rem;
  }
  details.abstract[open] summary {
    background-color: rgba(0,0,0,.03);
  }
  .paper-block { margin-bottom: 1.5rem; }
  .paper-title { font-weight: 600; }
  .paper-meta { color: #6c757d; }
---

## Working Papers

{% assign working_papers = 
  [
    {
      "title": "Coordinating Development Under Political Risk (Job Market Paper)",
      "authors": "with Mehdi Shadmehr",
      "pdf": "/assets/pdf/JMP_Coordinating_Development_Under_Political_Risk.pdf",
      "abstract": "Political risk and coordination failure are two leading causes of low investment and growth in low- and middle-income countries. The international community devotes substantial resources to addressing these challenges. We show that these problems are intertwined: political risk induces coordination failure. We then propose a subsidy program to eliminate politically induced miscoordination. Our program---Guaranteed Return with Profit- and Loss-Sharing (GPLS)---offers a minimum return to investors while clawing back returns above a specified maximum. The design screens out investors who would have invested even without subsidies and induces participation from more hesitant investors at minimal cost. Optimally designed GPLS programs significantly reduce costs relative to natural alternatives, such as guaranteed return schemes (e.g., fixed annual payments of $x$ per cent) or Guaranteed Return with Profit-Sharing (GPS) programs. Such optimal subsidies represent a major step toward feasible and sustainable international interventions to coordinate development under political risk."
    },
    {
      "title": "Strategic Investments Under Geopolitical Risks",
      "authors": "",
      "pdf": "/assets/pdf/Investments_Conflict_3 (9).pdf",
      "abstract": "How do firms account for the risk of war when making their investment decisions? How sensitive are countries to economic loss due to conflict? To what extent does global economic exchange deter conflict between countries? This paper re-visits the pacifying effect of global economic exchange by examining investment behavior in the presence of geopolitical risks. Much of the existing research on this topic analyzes the relationship between trade and military conflicts, with scholars divided on whether trade indeed pacifies. However, trade ties adapt to changing geopolitical scenario relatively easily. On the other hand, foreign investments are more sensitive to changing geopolitical risks as firms stand to suffer significant losses in the event of conflict. Understanding the relationship between investments and geopolitical risks is, therefore, crucial for gaining deeper insights about the dynamics between global economic exchange and inter-state conflicts. This paper employs a formal model to re-examine the pacifying effect of economic ties between countries. The formal model in this paper accounts for the inherent endogeneity of investment flows to inter-state conflict. By modeling this endogeneity, this paper provides a framework that more accurately captures how foreign investments affect geopolitical conflicts and, conversely, how these conflicts shape investment behavior."
    }
  ]
%}

{% for p in working_papers %}
<div class="paper-block">
  <div class="paper-title">{{ p.title }}</div>
  {% if p.authors != "" %}<div class="paper-meta">{{ p.authors }}</div>{% endif %}
  <div class="mt-1">
    {% comment %}
    {% if p.pdf %}
      <a class="btn btn-sm btn-outline-primary" href="{{ p.pdf | relative_url }}" target="_blank">PDF</a>
    {% endif %}
    {% endcomment %}
    <details class="abstract">
      <summary>Abstract</summary>
      <div class="mt-2">{{ p.abstract }}</div>
    </details>
  </div>
</div>
{% endfor %}

---

## Work in Progress

{% assign wip_papers = 
  [
    {
      "title": "Designing an Investment Screening Regime",
      "authors": "",
      "pdf": "/assets/pdf/Designing_Investment_Screening_Paper (1).pdf",
      "abstract": "This project examines the rise of investment screening mechanisms and develops a contract-theoretic model of how governments design optimal screening to mitigate security risks while preserving investment."
    },
    {
      "title": "Strategic Substitutes in Global Games",
      "authors": "",
      "pdf": "",
      "abstract": "This paper extends the global games framework to finite-player settings with strategic substitutes, studying conditions under which payoff asymmetries can generate unique equilibria."
    },
    {
      "title": "The Value of Intelligence in Conflict",
      "authors": "with Kris Ramsay",
      "pdf": "/assets/pdf/Blotto_2_on_1.pdf",
      "abstract": "Using a Blotto-style framework, this project analyzes how a defender allocates resources between direct defense and intelligence gathering when facing multiple attackers. It highlights the strategic value of costly intelligence in modern counter-terrorism."
    }
  ]
%}

{% for p in wip_papers %}
<div class="paper-block">
  <div class="paper-title">{{ p.title }}</div>
  {% if p.authors != "" %}<div class="paper-meta">{{ p.authors }}</div>{% endif %}
  <div class="mt-1">
    {% comment %}
    {% if p.pdf %}
      <a class="btn btn-sm btn-outline-primary" href="{{ p.pdf | relative_url }}" target="_blank">PDF</a>
    {% endif %}
    {% endcomment %}
    {% comment %}
    <details class="abstract">
      <summary>Abstract</summary>
      <div class="mt-2">{{ p.abstract }}</div>
    </details>
    {% endcomment %}
  </div>
</div>
{% endfor %}

