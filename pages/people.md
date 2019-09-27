---
layout: page
title: People
permalink: /people/
navbar-index: 1
---

{% assign profs = site.people | where: 'category', 'faculty' %}
{% assign students = site.people | where: 'category', 'stu' %}

## Faculty

{% for person in profs %}

<section class="profile">
  <img src="/assets/img/people/{{ person.photo }}.jpg" alt="Photo of {{ person.name }}">
  <div class="info">
    <a href="{{ person.website }}"><h3>{{ person.name }}</h3></a>
    <h4>{{ person.position }}</h4>
    <p>{{ person.content }}</p>
  </div>
</section>

{% endfor %}

{% assign grads = site.people | where: 'category', 'grad' %}

## Students

{% for person in students %}

<section class="profile">
  <img src="/assets/img/people/{{ person.photo }}.jpg" alt="Photo of {{ person.name }}">
  <div class="info">
    <a href="{{ person.website }}"><h3>{{ person.name }}</h3></a>
    <h4>{{ person.position }}</h4>
    <p>{{ person.content }}</p>
  </div>
</section>

{% endfor %}

{% assign grads = site.people | where: 'category', 'grad' %}

-------------------------------
<h1><center>Past Students</center></h1>
<font color="red"><b><p>Note that Dr. Irfan Ahmed (co-)supervised these students at his current and former institutions. We maintain this list to acknowledge their association with us.
    </p></b></font>
## Doctorate Research Assistants
-------------------------------
## Masters Research Assistants

{% for person in grads %}

<section class="profile">
  <img src="/assets/img/people/{{ person.photo }}.jpg" alt="Photo of {{ person.name }}">
  <div class="info">
    <a href="{{ person.website }}"><h3>{{ person.name }}</h3></a>
    <p>{{ person.content }}</p>
  </div>
</section>

{% endfor %}

{% assign undergrads = site.people | where: 'category', 'undergrad' %}

------------------------------------

## Undergraduate Research Assistants

{% for person in undergrads %}

<section class="profile">
  <img src="/assets/img/people/{{ person.photo }}.jpg" alt="Photo of {{ person.name }}">
  <div class="info">
    <a href="{{ person.website }}"><h3>{{ person.name }}</h3></a>
    <p>{{ person.content }}</p>
  </div>
</section>

{% endfor %}

{% assign past_members = site.people | where: 'category', 'past' %}

