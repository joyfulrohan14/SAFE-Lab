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

[About Us](/facility/)
-----------------
<p>Security and Forensics Engineering (SAFE) Lab is founded and directed by Dr. Irfan Ahmed in the Department of Computer Science at the College of Engineering at Virginia Commonwealth University. We work on a broad field of cybersecurity including the following:

<ul><li>Digital Forensics</li><ul>
<li>Memory Forensics </li>
<li>Code Fingerprinting</li>
<li>Cloud Forensics</li>
<li>File Type/Encoding Identification</li>
</ul>

<li>Industrial Control System (ICS) Security
</li><ul>
<li>Exploring new attack vectors
</li>
<li>Identifying Vulnerabilities
</li>
<li>Attack Detection and Recovery
/li>
<li>Digital Forensics Readiness, Tools and Techniques
</li>
</ul>

<li>Smart Manufacturing Security 
</li><ul>
<li>Digital Twin
 </li>
<li>3D Printers</li>
<li>Internet of Things
</li>
</ul>

<li>System Virtualization Security
</li><ul>
<li>Hypervisor 
 </li>
<li>Virtual Machine Introspection
</li>
<li>Lightweight Containers
</li>
</ul>

<li>Malware</li><ul>
<li>Software/Protocol Reverse Engineering
 </li>
<li>Malware Detection, Analysis, and Characterization
</li>
</ul>

<li>Human Aspects of Cybersecurity 
</li><ul>
<li>Studying and Improving (In)secure Cyber Behavior of End Users e.g., Personality Traits
 </li>
</ul>

The lab is fully-equipped with Desktop computers, laboratory-scale ICS testbeds of several vendors (including GE, Mitsubishi, Allen-Bradley, Siemens, Schneider Electric, Omron, WAGO, and AutomationDirect), 3D printers, and access to a data center of high-performance computing infrastructure. 


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
