---
layout: default
title: AI Summaries
---

# All AI Summaries

<ul>
  {% for page in site.pages %}
    {% if page.path contains 'summary_ai/' and page.url != '/summary_ai/' %}
      <li>
        <a href="{{ page.url | relative_url }}">
          {{ page.name | remove: ".md" }}
        </a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
