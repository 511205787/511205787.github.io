---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<style>
  .cv-publications-note {
    margin: 0 0 1.5rem;
    color: #746f63;
    font-size: 0.95rem;
    line-height: 1.7;
  }

  .cv-publication-list {
    margin-top: 1.5rem;
  }

  .publication-card {
    display: grid;
    gap: 1.5rem;
    margin-bottom: 2.5rem;
    padding-bottom: 2.2rem;
    border-bottom: 1px solid #ece5d4;
  }

  .publication-card:last-child {
    margin-bottom: 0;
    padding-bottom: 0;
    border-bottom: 0;
  }

  .publication-card--with-image {
    grid-template-columns: minmax(240px, 320px) minmax(0, 1fr);
    align-items: start;
  }

  .publication-card__media {
    overflow: hidden;
    border: 1px solid #efe9dc;
    border-radius: 1rem;
    background: linear-gradient(180deg, #fffdf8 0%, #f7f1e6 100%);
    box-shadow: 0 14px 32px rgba(88, 74, 35, 0.08);
  }

  .publication-card__image {
    display: block;
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  .publication-card__title {
    margin: 0 0 0.7rem;
    color: #2a2a2a;
    font-size: 1.75rem;
    line-height: 1.26;
  }

  .publication-card__authors,
  .publication-card__venue {
    margin: 0;
  }

  .publication-card__authors {
    color: #444;
    font-size: 1.08rem;
    line-height: 1.65;
  }

  .publication-card__venue {
    margin-top: 0.35rem;
    color: #605b52;
    font-size: 1.05rem;
    line-height: 1.6;
  }

  .publication-card__badges {
    margin: 0.75rem 0 0;
  }

  .publication-card__badge {
    display: inline-block;
    padding: 0.25rem 0.65rem;
    border: 1px solid #dbc78a;
    border-radius: 0.55rem;
    background: #fbf6e8;
    color: #8b6d1c;
    font-size: 0.92rem;
    font-weight: 700;
  }

  .publication-card__toggle {
    display: none;
  }

  .publication-card__link-row {
    margin-top: 0.9rem;
    color: #7d766a;
    font-size: 1rem;
    line-height: 1.7;
  }

  .publication-card__link-row a,
  .publication-card__toggle-label {
    color: #1f5f92;
    text-decoration: none;
  }

  .publication-card__link-row a:hover,
  .publication-card__toggle-label:hover {
    color: #0f4168;
  }

  .publication-card__toggle-label {
    cursor: pointer;
  }

  .publication-card__toggle-less {
    display: none;
  }

  .publication-card__toggle:checked ~ .publication-card__link-row .publication-card__toggle-more {
    display: none;
  }

  .publication-card__toggle:checked ~ .publication-card__link-row .publication-card__toggle-less {
    display: inline;
  }

  .publication-card__abstract {
    display: none;
    margin-top: 1rem;
    color: #333;
    font-size: 1.02rem;
    line-height: 1.85;
  }

  .publication-card__abstract p {
    margin: 0;
  }

  .publication-card__toggle:checked ~ .publication-card__abstract {
    display: block;
  }

  .publication-card__sep {
    margin: 0 0.3rem;
    color: #9d9587;
  }

  @media (max-width: 900px) {
    .publication-card--with-image {
      grid-template-columns: 1fr;
    }

    .publication-card__title {
      font-size: 1.4rem;
    }
  }
</style>

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
<p class="cv-publications-note">First-author works are highlighted in the author list.</p>

<div class="cv-publication-list">
{% assign publications_sorted = site.publications | sort: "date" | reverse %}
{% for post in publications_sorted %}
  {% include archive-single-publication-card.html %}
{% endfor %}
</div>


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
