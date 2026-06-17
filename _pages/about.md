---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="snowball-home">
  <section class="snowball-home__hero">
    <aside class="snowball-home__panel snowball-home__profile">
      <div class="snowball-home__photo">
        <img src="{{ base_path }}/images/{{ site.author.avatar }}" alt="{{ site.author.name }}">
      </div>
      <div>
        <h1 class="snowball-home__name">{{ site.author.name }}</h1>
        <p class="snowball-home__affiliation">William &amp; Mary</p>
        <p class="snowball-home__role">Second year Ph.D student</p>
      </div>
      <div class="snowball-home__links" aria-label="Profile links">
        <a class="snowball-home__link" href="mailto:{{ site.author.email }}">Email</a>
        <a class="snowball-home__link" href="{{ base_path }}/assets/CV.pdf">CV</a>
        <a class="snowball-home__link" href="{{ site.author.googlescholar }}">Scholar</a>
        <a class="snowball-home__link" href="https://github.com/{{ site.author.github }}">GitHub</a>
      </div>
    </aside>

    <section class="snowball-home__panel snowball-home__intro" aria-labelledby="brief-heading">
      <p class="snowball-home__eyebrow">Brief</p>
      <div id="brief-heading">
        <p>I'm a second year phd student from William & Mary, advised by Professor <a href="https://huajieshao.github.io/index.html">Huajie Shao</a>. My current research interest focuses on developing physics‑informed machine learning methods to build generalizable world models, with applications spanning robotics, autonomous driving, and power systems.</p>
        <p>You can find my CV here: <a href="{{ base_path }}/assets/CV.pdf">Yuchen Wang's Curriculum Vitae</a>.</p>
      </div>
    </section>
  </section>

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
    <ul class="about-section__list">
      <li class="about-section__item">2026 — First-author paper “WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotic Systems” was accepted to ICML 2026 as a <strong>spotlight (top 2.2%)</strong>.</li>
      <li class="about-section__item">2026 — First-author paper “WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotics” was accepted to the ICLR 2026 Workshop on World Models: Understanding, Modelling and Scaling.</li>
      <li class="about-section__item">2026 — Co-author paper “A Generalizable Physics-guided Causal Model for Trajectory Prediction in Autonomous Driving” was accepted to ICRA 2026.</li>
      <li class="about-section__item">2025 — First-author paper “A Generalizable Physics-Enhanced State Space Model for Long-Term Dynamics Forecasting in Complex Environments” was accepted to <a href="https://icml.cc/virtual/2025/poster/46230">ICML 2025</a>.</li>
      <li class="about-section__item">2025 — Co-author paper “Accelerating Neural ODEs: A Variational Formulation-based Approach” was accepted to <a href="https://openreview.net/forum?id=trV41CpAK4">ICLR 2025</a>.</li>
    </ul>

    <details class="about-section__details">
      <summary>
        <span class="about-section__more">Show More</span>
        <span class="about-section__less">Show Less</span>
      </summary>
      <ul class="about-section__list about-section__extra">
        <li class="about-section__item">2024 — First-author paper “A Deep Transfer Operator Learning Method for Temperature Field Reconstruction in a Lithium-Ion Battery Pack” was published in <a href="https://ieeexplore.ieee.org/abstract/document/10462637">IEEE Transactions on Industrial Informatics</a>.</li>
        <li class="about-section__item">2024 — Co-author paper “Accelerating Neural Differential Equations for Irregularly-Sampled Dynamical Systems Using Variational Formulation” was presented at the <a href="https://openreview.net/forum?id=C8tlOCzqll&noteId=l7nUWhiwog">ICLR 2024 Workshop on AI4DifferentialEquations In Science</a>.</li>
        <li class="about-section__item">2024 — Awarded Outstanding Graduate Award, Shanghai Jiao Tong University.</li>
        <li class="about-section__item">2023 — First-author paper “Temperature State Prediction for Lithium-ion Batteries Based on Improved Physics-Informed Neural Networks” was published in <a href="https://www.sciencedirect.com/science/article/abs/pii/S2352152X23022600">Journal of Energy Storage</a>.</li>
      </ul>
    </details>
  </section>

  <section class="about-section">
    <h2 class="about-section__title">Honors & Awards</h2>
    <ul class="about-section__list">
      {% for item in site.data.profile.honors limit:4 %}
      <li class="about-section__item">{{ item }}</li>
      {% endfor %}
    </ul>

    <details class="about-section__details">
      <summary>
        <span class="about-section__more">Show More</span>
        <span class="about-section__less">Show Less</span>
      </summary>
      <ul class="about-section__list about-section__extra">
        {% for item in site.data.profile.honors offset:4 %}
        <li class="about-section__item">{{ item }}</li>
        {% endfor %}
      </ul>
    </details>
  </section>

  <section class="about-section">
    <h2 class="about-section__title">Services</h2>
    <p class="about-section__service"><span class="about-section__label">Conference Reviewer:</span> {% for item in site.data.profile.services.conference %}{{ item.text }}{% if item.note %} ({% if item.note_strong %}<strong>{{ item.note }}</strong>{% else %}{{ item.note }}{% endif %}){% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}</p>
    <p class="about-section__service"><span class="about-section__label">Workshop Reviewer:</span> {% for item in site.data.profile.services.workshop %}{{ item.text }}{% unless forloop.last %}, {% endunless %}{% endfor %}</p>
  </section>
</div>
