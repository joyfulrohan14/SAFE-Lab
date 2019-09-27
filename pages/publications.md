---
layout: page
title: Publications
permalink: /publications/
navbar-index: 2
---

<h3><a href="/publications/by-date/">Sort by date</a></h3>

Journals/Book Chapters
----------------------

<ul>
{% assign journals = site.publications | where: 'type', 'journal' | sort: 'date' | reverse %}

{% for pub in journals %}
  <li>
    <p>
      {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}">“ {{ pub.title }} ”</a>
      {% else %}
        “ {{ pub.title }} ”
      {% endif %}
      , {{ pub.published-by }}
      , {{ pub.published-in }}
      {% if pub.note %}, ( {{ pub.note }} ){% endif %}
        <br>
      {% if pub.file %}
            <a href = "{{ pub.file }}" target="_blank"> [PDF] </a>
      {% endif %}
        {% if pub.bibtext %}
            <a href = "{{ pub.bibtext }}" target="_blank"> [Bibtext] </a>
      {% endif %}
    </p>
  </li>
{% endfor %}
</ul>

Conferences/Workshops
---------------------

<ul>
{% assign conferences = site.publications | where: 'type', 'conference' | sort: 'date' | reverse %}

{% for pub in conferences %}
  <li>
    <p>
        {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}">“ {{ pub.title }} ”</a>
      {% else %}
        “ {{ pub.title }} ”
      {% endif %}
      , {{ pub.published-by }}
      , {{ pub.published-in }}
      , {{ pub.venue }}
      {% if pub.note %}, ( {{ pub.note }} ){% endif %}
        <br>
      {% if pub.file %}
            <a href = "{{ pub.file }}" target="_blank"> [PDF] </a>
      {% endif %}
        {% if pub.bibtext %}
            <a href = "{{ pub.bibtext }}" target="_blank"> [Bibtext] </a>
      {% endif %}
    </p>
  </li>
{% endfor %}
</ul>
