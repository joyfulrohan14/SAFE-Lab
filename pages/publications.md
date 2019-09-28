---
layout: page
title: Publications
permalink: /publications/
navbar-index: 2
---

<h3><center><a href="/publications/by-date/">Sort by date</a></center></h3>
<hr>

Journals/Book Chapters
----------------------


<ul>
{% assign journals = site.publications | where: 'type', 'journal' | sort: 'date' | reverse %}

{% for pub in journals %}
  <li>
    <p>
      {% if pub.abbrv %} <b>[{{ pub.abbrv }}]: </b>{% endif %}
      {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}" target="_blank">“ {{ pub.title }} ”</a>
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

<hr>

Conferences/Workshops
---------------------

<ul>
{% assign conferences = site.publications | where: 'type', 'conference' | sort: 'date' | reverse %}

{% for pub in conferences %}
  <li>
    <p>
        {% if pub.abbrv %} <b>[{{ pub.abbrv }}]: </b>{% endif %}
        {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}" target="_blank">“ {{ pub.title }} ”</a>
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

Posters/Extended Abstracts/Work-in-progress Presentations:
---------------------

<ul>
{% assign conferences = site.publications | where: 'type', 'wip' | sort: 'date' | reverse %}

{% for pub in conferences %}
  <li>
    <p>
        {% if pub.abbrv %} <b>[{{ pub.abbrv }}]: </b>{% endif %}
        {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}" target="_blank">“ {{ pub.title }} ”</a>
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


Other Publications:
---------------------

<ul>
{% assign journals = site.publications | where: 'type', 'other' | sort: 'date' | reverse %}

{% for pub in journals %}
  <li>
    <p>
      {% if pub.abbrv %} <b>[{{ pub.abbrv }}]: </b>{% endif %}
      {% for author in pub.authors %}
        {{ author }},
      {% endfor %}
      {% if pub.file %}
        <a href="{{ pub.file }}" target="_blank">“ {{ pub.title }} ”</a>
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

<hr>


