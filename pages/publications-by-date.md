---
layout: page
title: Publications
permalink: /publications/by-date/
---

<h3><center><a href="/publications/">Group by type</a></center></h3>

<ul>
{% assign pubs = site.publications | sort: 'date' | reverse %}


 {% assign year = "None" %}


{% for pub in pubs %}


  {% if year != pub.year and pub.year > 2015 %}
   <hr>
   <h3><b>[{{ pub.year }}] </b></h3>
    {% assign year = pub.year %}
  {% endif %}
 
  {% if year != pub.year and year == 2016 %}
   <hr>
   <h3><b>[2015 and Before] </b></h3>
    {% assign year = pub.year %}
  {% endif %}
 
  <li>
    <p>
      {% if pub.abbrv %} <b>[{{ pub.abbrv }}]: </b>{% endif %}
      {% for author in pub.authors %} {{ author }}, {% endfor %}
      {% if pub.file %} <a href=" {{ pub.file }} " target="_blank"> “ {{ pub.title }} ” </a> {% else %} “ {{ pub.title }} ” {% endif %},
      {{ pub.published-by }},
      {{ pub.published-in }}
      {% if pub.note %}, ({{ pub.note }}){% endif %}
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
