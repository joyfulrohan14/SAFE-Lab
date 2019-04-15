---
layout: default
title: Home
permalink: /
navbar-index: 0
---

<div class="carousel">
  <div><figure><img src="/assets/img/sprites/lab.jpg" alt="lab facility"><figcaption>Lab Facility</figcaption></figure></div>
  <div><figure><img src="/assets/img/sprites/lab.jpg" alt="lab facility"><figcaption>Lab Facility</figcaption></figure></div>
  
</div>

<aside class="home-page-aside">
    <article class="photo-frame">
        <h2><a href="/news/">News</a></h2>
        <ul class="post-list">
        {% for post in site.posts limit: 3 %}
          <li>
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            <h4>
              <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | truncate: 50}}</a>
            </h4>
          </li>
        {% endfor %}
        </ul>

        <a href="/news/"> More News...</a>
    </article>
    <hr>
    <article class="photo-frame publication">
        <h2><a href="/publications/">Publications</a></h2>

        <ul class="post-list">
        {% assign pubs = site.publications | sort: 'date' | reverse %}

        {% for pub in pubs limit: 3%}
          <li>
            <p>
              {% for author in pub.authors %} {{ author }}, {% endfor %}
              {% if pub.file %} <a href=" {{ pub.file }} "> “ {{ pub.title | truncate: 50 }} ” </a> {% else %} “ {{ pub.title | truncate: 50 }} ” {% endif %}
            </p>
          </li>
        {% endfor %}
        </ul>

        <a href="/publications/"> More Publications...</a>
    </article>
</aside>

[About CyPhy Lab](/facility/)
-----------------

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi a orci id ante malesuada auctor. Duis feugiat iaculis malesuada. Vestibulum feugiat vestibulum lectus, non lobortis magna. In a porttitor eros. Duis diam mi, varius ac sem at, sodales varius nibh. Nunc quis euismod quam. Nunc at auctor neque, eget facilisis diam. Aenean vel lectus eget dolor eleifend fringilla maximus sit amet leo. Nunc eget felis quis ante aliquet dictum ut id lacus...

[More about the facility...](/facility/)

<div class="quick-info">
    <h2><a href="http://gnocia.cs.uno.edu/" class="external" target="_blank">GNOCIA</a></h2>
    <p>The University of New Orleans has the strongest Information Assurance (IA) program in the region and is designated as a National Center of Academic Excellence (CAE) in Information Assurance Education (CAE) and in Information Assurance Research (CAE-R) by the National Security Agency (NSA) and the Department of Homeland Security (DHS)—the only university holding these designations in the State of Louisiana...</p>
    <p><a href="http://gnocia.cs.uno.edu/" target="_blank">Go to GNOCIA's website...</a></p>
</div>

<div class="quick-info">
    <h2><a href="http://www.uno.edu/cos/computer-science/information-assurance.aspx" class="external">Information Assurance at UNO</a></h2>
    <p>The University of New Orleans has the strongest Information Assurance (IA) program in the region and is designated as a National Center of Academic Excellence (CAE) in Information Assurance Education (CAE) and in Information Assurance Research (CAE-R) by the National Security Agency (NSA) and the Department of Homeland Security (DHS)—the only university holding these designations in the State of Louisiana...</p>
    <p><a href="http://www.uno.edu/cos/computer-science/information-assurance.aspx" target="_blank">More about Information Assurance at UNO...</a></p>
</div>

<div class="sponsors">
    <h2>Our Sponsors</h2>
    <ul class="sponsors">
        <li><a href="https://www.nsf.gov/"><img src="/assets/img/sponsors/nsf.png"></a></li>
        <li><a href="http://www.onr.navy.mil/"><img src="/assets/img/sponsors/onr.png"></a></li>
        <li><a href="http://www.onr.navy.mil/"><img src="/assets/img/sponsors/onr1.png"></a></li>
        <li><a href="http://www.arl.army.mil/www/default.cfm?page=29"><img src="/assets/img/sponsors/aro.png"></a></li>
    </ul>
</div>

<script src="/assets/js/jquery-3.1.0.min.js"></script>
<script src="/assets/js/slick.min.js"></script>
<script>
    $(document).ready(function(){
      $('.carousel').slick({
          autoplay: true,
          dots: true
      });
    });
</script>
