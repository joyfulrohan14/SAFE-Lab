---
layout: page
title: Publications
permalink: /publications/by-date/
---

<h3><a href="/publications/">Group by type</a></h3>

<ul>
{% assign pubs = site.publications | sort: 'date' | reverse %}

{% for pub in pubs %}
  <li>
    <p>
      {% for author in pub.authors %} {{ author }}, {% endfor %}
      {% if pub.file %} <a href=" {{ pub.file }} "> “ {{ pub.title }} ” </a> {% else %} “ {{ pub.title }} ” {% endif %},
      {{ pub.published-by }},
      {{ pub.published-in }}
      {% if pub.note %}, ({{ pub.note }}){% endif %}
      {% if pub.file %}
        {% assign type = pub.file | split: '.' %}
        <a href=" {{ pub.file }}" class="{{ type.last }}"></a>
      {% endif %}
    </p>
  </li>
{% endfor %}
</ul>
