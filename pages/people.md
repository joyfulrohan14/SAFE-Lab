---
layout: page
title: People
permalink: /people/
navbar-index: 1
---

{% assign profs = site.people | where: 'category', 'faculty' %}

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

-------------------------------

## Graduate Research Assistants

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

--------------------

## Past Lab Members

{% for member in past_members %}

{{ member.content }}

{% endfor %}