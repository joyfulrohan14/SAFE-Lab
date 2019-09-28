---
layout: default
title: Home
permalink: /
navbar-index: 0
---

<div class="carousel">
  <div><figure><img src="/assets/img/sprites/lab.jpg" alt="SAFE Lab Space"><figcaption>SAFE Lab Space</figcaption></figure></div>
  <div><figure><img src="/assets/img/sprites/powe-award.jpg" alt="lab facility"><figcaption>Ralph E. Powe Junior Faculty Enhancement Awards</figcaption></figure></div>
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

### About Us
-----------------
**Security and Forensics Engineering (SAFE) Lab** is founded and directed by Dr. Irfan Ahmed in the Department of Computer Science at the College of Engineering at Virginia Commonwealth University. 

The lab focuses on a broad field of <span style="color:red">Cybersecurity</span> including the following:

* **Digital Forensics**
	- Memory Forensics
	- Code Fingerprinting
	- Cloud Forensics
	- File Type/Encoding Identification


* **Industrial Control System (ICS) Security**
	- Exploring new attack vectors
    - Identifying Vulnerabilities
    - Attack Detection and Recovery
    - Digital Forensics Readiness, Tools and Techniques

* **Smart Manufacturing Security**
    - Digital Twin
    - 3D Printers</li>
    - Internet of Things


* **System Virtualization Security**
    - Hypervisor 
    - Virtual Machine Introspection
    - Lightweight Containers


* **Malware**
    - Software/Protocol Reverse Engineering
    - Malware Detection, Analysis, and Characterization


* **Human Aspects of Cybersecurity**
    - Studying and Improving (In)secure Cyber Behavior of End Users e.g., Personality Traits


The lab is fully-equipped with Desktop computers, laboratory-scale ICS testbeds of several vendors (including GE, Mitsubishi, Allen-Bradley, Siemens, Schneider Electric, Omron, WAGO, and AutomationDirect), 3D printers, and access to a data center of high-performance computing infrastructure. 


<div class="sponsors">
    <h2>Our Sponsors</h2>
    <ul class="sponsors">
        <li><a href="https://www.nsf.gov/"><img src="/assets/img/sponsors/nsf.png"></a></li>
        <li><a href="http://www.onr.navy.mil/"><img src="/assets/img/sponsors/orau.jpg"></a></li>
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
