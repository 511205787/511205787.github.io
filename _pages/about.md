---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a second year phd student from William & Mary, advised by Professor [Huajie Shao](https://huajieshao.github.io/index.html). My current research interest focuses on developing physics‑informed machine learning methods to build generalizable world models, with applications spanning robotics, autonomous driving, and power systems.

You can find my CV here: [Yuchen Wang's Curriculum Vitae](../assets/CV.pdf).

<style>
  .page__title {
    margin-bottom: 1.15rem;
    color: #b59a4a;
  }

  .page__title::after {
    content: "";
    display: block;
    width: 3rem;
    height: 0.2rem;
    margin-top: 0.45rem;
    border-radius: 999px;
    background: linear-gradient(90deg, #b59a4a 0%, #d8c693 100%);
  }

  .about-section {
    margin-top: 2.75rem;
    padding-top: 1.5rem;
    border-top: 1px solid #e7e0cf;
  }

  .about-section--first {
    margin-top: 2.25rem;
  }

  .about-section__title {
    margin: 0 0 1.15rem;
    color: #b59a4a;
    font-size: 2.15rem;
    font-weight: 700;
    letter-spacing: -0.03em;
    line-height: 1.05;
  }

  .about-section__title::after {
    content: "";
    display: block;
    width: 3rem;
    height: 0.2rem;
    margin-top: 0.45rem;
    border-radius: 999px;
    background: linear-gradient(90deg, #b59a4a 0%, #d8c693 100%);
  }

  .about-section__list {
    margin: 0;
    padding-left: 1.5rem;
  }

  .about-section__item {
    margin-bottom: 0.5rem;
  }

  .about-section__item:last-child {
    margin-bottom: 0;
  }

  .about-section__details {
    margin-top: 0.35rem;
  }

  .about-section__details summary {
    display: inline-block;
    cursor: pointer;
    color: #7a7466;
    font-weight: 500;
    list-style: none;
  }

  .about-section__details summary::-webkit-details-marker {
    display: none;
  }

  .about-section__details summary:hover {
    color: #2f2f2f;
  }

  .about-section__extra {
    margin-top: 0.5rem;
  }

  .about-section__less {
    display: none;
  }

  .about-section__details[open] {
    display: flex;
    flex-direction: column;
  }

  .about-section__details[open] .about-section__extra {
    order: 1;
  }

  .about-section__details[open] summary {
    order: 2;
    margin-top: 0.35rem;
  }

  .about-section__details[open] .about-section__more {
    display: none;
  }

  .about-section__details[open] .about-section__less {
    display: inline;
  }

  .about-section__service {
    margin: 0 0 0.7rem;
    line-height: 1.75;
  }

  .about-section__service:last-child {
    margin-bottom: 0;
  }

  .about-section__label {
    color: #2f2f2f;
    font-weight: 700;
  }
</style>

<section class="about-section about-section--first">
  <h2 class="about-section__title">Education</h2>
  <ul class="about-section__list">
    {% for item in site.data.profile.education.about %}
    <li class="about-section__item">{{ item }}</li>
    {% endfor %}
  </ul>
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

<section class="about-section">
  <h2 class="about-section__title">Contact Information</h2>
  <ul class="about-section__list">
    {% for item in site.data.profile.contact %}
    <li class="about-section__item">{{ item.label }}: {{ item.value }}</li>
    {% endfor %}
  </ul>
</section>
