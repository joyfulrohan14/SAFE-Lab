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

## Current Students

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
<center><font color="red"><b><p>Note that Dr. Irfan Ahmed (co-)supervised these students at his current and former institutions. We maintain this list to acknowledge their association with us.
    </p></b></font></center>
    
-------------------------------
### Postdoctoral Research Associates
* **Hyunguk Yoo**
	- PhD from Ajou University, South Korea
	- Current employment: Assistant Professor at University of New Orleans
	
-------------------------------

### Doctorate Research Assistants
* **Aisha Ibrahim Ali-Gombe**
	- Thesis Title: Malware Analysis and Privacy Policy Enforcement Techniques for Android Applications
	- First employment: Assistant Professor at Towson University, MD
	
* **Eesa Alsolami**
	- Thesis Title: Continuous Biometric Authentication: Keystroke Dynamics
	- First employment: Assistant Professor at University of Jeddah, Saudi Arabia



-------------------------------

### Masters Research Assistants

* **Pranita Deshpande**
	- Thesis Title: Assessment of Two Pedagogical Tools for Cybersecurity Education
	- Publications: ACM SIGCSE'19 (a), and ACM SIGCSE'19 (b)

* **Sharon Elizabeth Blake**
	- Thesis Title: MAnanA: A Heuristic Scoring Framework for Concept Map Analysis in Cybersecurity Education
	- Publications: -

* **Sushma Kalle**
	- Thesis Title: Semantic-aware Stealthy Control Logic Infection Attack
	- Publications: NDSS BAR'19, and DIMVA'19
	
* **Jonathan Grimm**
	- Thesis Title: Automatic Mitigation of Kernel Rootkits in Cloud Environments
	- Publications: WISA'18 
	
* **Saranyan Senthivel**
	- Thesis Title: Automatic Forensic Analysis of PCCC Network Traffic Log
	- Publications: ACSAC ICSS'16, DFRWS'17, and CODASPY'18
	
* **William Eldon Johnson**
	- Thesis Title: Development of Peer Instruction Material for a Cybersecurity Curriculum
	- Publications: ACSAC ICSS'16, USENIX ASE'16, and USENIX ASE'17
	
* **Anjila Tamrakar**
	- Thesis Title: SPICE: A Software Tool for Studying End-user's Insecure Cyber Behavior and Personality-traits}\\
	- Publications: CODASPY'18

* **Dalbir Kaur Chhabra**
	- Thesis Title: Feature selection and clustering for malicious and benign software characterization
	- Publications: -


------------------------------------

### Undergraduate Research Assistants

* **Jose Rene Berlioz Rivera**
* **Shrey Dhungana**
	- Publications: CODASPY'18 
* **Nabeel Gulzar Rana**
* **Manish Bhatt**
	- Publications: WISA'17, SIGCSE'18, and DFRWS'18
* **Banan Ibrahim**
* **Phillip Bradley Reason**
* **Philip Schwartz**