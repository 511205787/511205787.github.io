---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======  
{% for item in site.data.profile.education.cv %}* {{ item }}  
{% endfor %}

  
<!-- Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3 -->

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>


Honors & Awards
======
{% for item in site.data.profile.honors %}* {{ item }}  
{% endfor %}

Services
======
* **Conference Reviewer:** {% for item in site.data.profile.services.conference %}{{ item.text }}{% if item.note %} ({% if item.note_strong %}**{{ item.note }}**{% else %}{{ item.note }}{% endif %}){% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}  
* **Workshop Reviewer:** {% for item in site.data.profile.services.workshop %}{{ item.text }}{% unless forloop.last %}, {% endunless %}{% endfor %}  

<!-- Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams -->
