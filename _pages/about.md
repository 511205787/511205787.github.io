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
      <div class="about-news-year">
        <span class="about-news-rail-mark" aria-hidden="true"></span>
        <span>2026</span>
      </div>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2026</span>Co-author paper <strong>“Lens: A Knowledge-Guided Foundation Model for Network Traffic”</strong> was accepted to <a class="about-news-venue" href="https://openreview.net/forum?id=cGDwTgnJIR">Transactions on Machine Learning Research (TMLR)</a>.</p>
      </article>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2026</span>First-author paper <strong>“WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotic Systems”</strong> was accepted to <span class="about-news-venue">ICML 2026</span> as a <span class="about-news-spotlight">spotlight (top 2.2%)</span>.</p>
      </article>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2026</span>First-author paper <strong>“WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotics”</strong> was accepted to the <span class="about-news-venue">ICLR 2026 Workshop on World Models: Understanding, Modelling and Scaling</span>.</p>
      </article>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2026</span>Co-author paper <strong>“A Generalizable Physics-guided Causal Model for Trajectory Prediction in Autonomous Driving”</strong> was accepted to <span class="about-news-venue">ICRA 2026</span>.</p>
      </article>
      <div class="about-news-year">
        <span class="about-news-rail-mark" aria-hidden="true"></span>
        <span>2025</span>
      </div>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2025</span>First-author paper <strong>“A Generalizable Physics-Enhanced State Space Model for Long-Term Dynamics Forecasting in Complex Environments”</strong> was accepted to <a class="about-news-venue" href="https://icml.cc/virtual/2025/poster/46230">ICML 2025</a>.</p>
      </article>
      <article class="about-news-item">
        <span class="about-news-node" aria-hidden="true"></span>
        <p><span class="about-news-date">2025</span>Co-author paper <strong>“Accelerating Neural ODEs: A Variational Formulation-based Approach”</strong> was accepted to <a class="about-news-venue" href="https://openreview.net/forum?id=trV41CpAK4">ICLR 2025</a>.</p>
      </article>
      <details class="about-section__details about-news-more">
        <summary class="about-news-toggle">
          <span class="about-section__more">Show More</span>
          <span class="about-section__less">Show Less</span>
        </summary>
        <div class="about-news-year">
          <span class="about-news-rail-mark" aria-hidden="true"></span>
          <span>2024</span>
        </div>
        <article class="about-news-item">
          <span class="about-news-node" aria-hidden="true"></span>
          <p><span class="about-news-date">2024</span>First-author paper <strong>“A Deep Transfer Operator Learning Method for Temperature Field Reconstruction in a Lithium-Ion Battery Pack”</strong> was published in <a class="about-news-venue" href="https://ieeexplore.ieee.org/abstract/document/10462637">IEEE Transactions on Industrial Informatics</a>.</p>
        </article>
        <article class="about-news-item">
          <span class="about-news-node" aria-hidden="true"></span>
          <p><span class="about-news-date">2024</span>Co-author paper <strong>“Accelerating Neural Differential Equations for Irregularly-Sampled Dynamical Systems Using Variational Formulation”</strong> was presented at the <a class="about-news-venue" href="https://openreview.net/forum?id=C8tlOCzqll&noteId=l7nUWhiwog">ICLR 2024 Workshop on AI4DifferentialEquations In Science</a>.</p>
        </article>
        <article class="about-news-item">
          <span class="about-news-node" aria-hidden="true"></span>
          <p><span class="about-news-date">2024</span>Awarded <strong>Outstanding Graduate Award, Shanghai Jiao Tong University</strong>.</p>
        </article>
        <div class="about-news-year">
          <span class="about-news-rail-mark" aria-hidden="true"></span>
          <span>2023</span>
        </div>
        <article class="about-news-item">
          <span class="about-news-node" aria-hidden="true"></span>
          <p><span class="about-news-date">2023</span>First-author paper <strong>“Temperature State Prediction for Lithium-ion Batteries Based on Improved Physics-Informed Neural Networks”</strong> was published in <a class="about-news-venue" href="https://www.sciencedirect.com/science/article/abs/pii/S2352152X23022600">Journal of Energy Storage</a>.</p>
        </article>
      </details>
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
