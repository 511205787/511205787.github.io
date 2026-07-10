---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

I'm a second year phd student from William & Mary, advised by Professor [Huajie Shao](https://huajieshao.github.io/index.html). My current research interest focuses on developing physics‑informed machine learning methods to build generalizable world models, with applications spanning robotics, autonomous driving, and power systems.

You can find my CV here: [Yuchen Wang's Curriculum Vitae](../assets/CV.pdf).

<div class="about-home">
  <section class="about-section about-section--first">
  <h2 class="about-section__title">Education</h2>
  <div class="about-education">
    {% for item in site.data.profile.education.about %}
    {% assign about_degree = item.degrees.first %}
    {% assign track_label = "Study" %}
    {% if about_degree.name contains "Ph.D." %}
      {% assign track_label = "Doctoral Study" %}
    {% elsif about_degree.name contains "M.S." %}
      {% assign track_label = "Master's Study" %}
    {% elsif about_degree.name contains "B.E." %}
      {% assign track_label = "Undergraduate Study" %}
    {% endif %}
    <article class="about-education__entry">
      <div class="about-education__main">
        <div class="about-education__logo-wrap">
          <img class="about-education__logo" src="{{ base_path }}/images/{{ item.logo }}" alt="{{ item.school }}">
        </div>
        <div class="about-education__copy">
          <div class="about-education__topline">
            <span class="about-education__track">{{ track_label }}</span>
            <div class="about-education__dates">
              {% for degree in item.degrees %}
              <span class="about-education__date">{{ degree.date }}</span>
              {% endfor %}
            </div>
          </div>
          <div>
            <h3 class="about-education__school">{{ item.school }}</h3>
            {% for degree in item.degrees %}
            <p class="about-education__degree">{{ degree.name }}</p>
            {% endfor %}
            <p class="about-education__location">{{ item.location }}</p>
          </div>
        </div>
      </div>
    </article>
    {% endfor %}
  </div>
  </section>

  <section class="about-section">
    <h2 class="about-section__title">News</h2>
    <div class="about-news-timeline">
      {%- assign news_visible = site.data.profile.news_visible | default: 5 -%}
      {%- assign news_year = "" -%}
      {%- assign news_folded = false -%}
      {%- for item in site.data.profile.news -%}
        {%- if forloop.index0 == news_visible and site.data.profile.news.size > news_visible -%}
      <details class="about-section__details about-news-more">
        <summary class="about-news-toggle">
          <span class="about-section__more">Show More</span>
          <span class="about-section__less">Show Less</span>
        </summary>
          {%- assign news_folded = true -%}
        {%- endif -%}
        {%- assign item_year = item.year | append: "" -%}
        {%- if item_year != news_year -%}
      <div class="about-news-year">
        <span class="about-news-rail-mark" aria-hidden="true"></span>
        <span>{{ item.year }}</span>
      </div>
          {%- assign news_year = item_year -%}
        {%- endif -%}
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">{{ item.year }}</span>{{ item.body }}</p>
      </article>
      {%- endfor -%}
      {%- if news_folded %}
      </details>
      {%- endif %}
    </div>
  </section>

  <section class="about-section">
    <h2 class="about-section__title">Honors & Awards</h2>
    <div class="about-award-list">
      {% for item in site.data.profile.honors limit:4 %}
      {% assign award_parts = item | split: "—" %}
      <article class="about-award-item">
        <time>{{ award_parts.last | strip }}</time>
        <p>{{ item }}</p>
      </article>
      {% endfor %}
      <input id="about-awards-toggle" class="about-awards-toggle-input" type="checkbox">
      {% for item in site.data.profile.honors offset:4 %}
      {% assign award_parts = item | split: "—" %}
      <article class="about-award-item about-award-item--extra">
        <time>{{ award_parts.last | strip }}</time>
        <p>{{ item }}</p>
      </article>
      {% endfor %}
      <label class="about-awards-toggle" for="about-awards-toggle">
        <span class="about-section__more">Show More</span>
        <span class="about-section__less">Show Less</span>
      </label>
    </div>
  </section>

  <section class="about-section">
    <h2 class="about-section__title">Services</h2>
    <div class="about-service-grid">
      <article class="about-service-card">
        <span class="about-service-card__label">Conference Reviewer</span>
        <p>{% for item in site.data.profile.services.conference %}{{ item.text }}{% if item.note %} ({% if item.note_strong %}<strong>{{ item.note }}</strong>{% else %}{{ item.note }}{% endif %}){% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}</p>
      </article>
      <article class="about-service-card">
        <span class="about-service-card__label">Workshop Reviewer</span>
        <p>{% for item in site.data.profile.services.workshop %}{{ item.text }}{% unless forloop.last %}, {% endunless %}{% endfor %}</p>
      </article>
    </div>
  </section>
</div>
