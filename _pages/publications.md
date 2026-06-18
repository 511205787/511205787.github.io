---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
  .publications-note {
    margin: 0 0 1.5rem;
    color: var(--snow-text-muted);
    font-size: 0.98rem;
    line-height: 1.8;
    font-style: normal;
  }

  .publication-list {
    margin-top: 1.75rem;
  }

  .publication-filters {
    display: flex;
    flex-wrap: wrap;
    gap: 0.9rem;
    margin: 1.35rem 0 1.2rem;
  }

  .publication-filters__input,
  .publication-filters__select {
    min-height: 3rem;
    border: 1px solid rgba(244, 240, 232, 0.22);
    border-radius: 0.8rem;
    background: #111720;
    color: #fffaf0;
    font: inherit;
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.045);
    transition: border-color 180ms ease, box-shadow 180ms ease, background 180ms ease;
  }

  .publication-filters__input::placeholder {
    color: rgba(255, 250, 240, 0.52);
  }

  .publication-filters__input:focus,
  .publication-filters__select:focus {
    border-color: rgba(214, 161, 95, 0.68);
    background: #151d23;
    box-shadow:
      inset 0 1px 0 rgba(255, 255, 255, 0.055),
      0 0 0 3px rgba(214, 161, 95, 0.14);
    outline: 0;
  }

  .publication-filters__input {
    flex: 1 1 18rem;
    padding: 0.8rem 1rem;
  }

  .publication-filters__select {
    min-width: 9rem;
    padding: 0.8rem 2.6rem 0.8rem 1rem;
  }

  .publication-filters__select option {
    background: #111720;
    color: #fffaf0;
  }

  .publication-filters__clear {
    min-height: 3rem;
    padding: 0.8rem 1.2rem;
    border: 1px solid rgba(244, 240, 232, 0.22);
    border-radius: 0.8rem;
    background: #111720;
    color: #fffaf0;
    cursor: pointer;
    font: inherit;
    transition: border-color 180ms ease, box-shadow 180ms ease, color 180ms ease, background 180ms ease;
  }

  .publication-filters__clear:hover {
    color: #fffaf0;
    border-color: rgba(214, 161, 95, 0.68);
    background: #151d23;
    box-shadow: 0 0 0 3px rgba(214, 161, 95, 0.12);
  }

  .publication-empty {
    display: none;
    margin-top: 1rem;
    color: var(--snow-text-muted);
    font-size: 0.98rem;
  }

  .publication-card {
    display: grid;
    gap: 1.5rem;
    margin-bottom: 2.5rem;
    padding-bottom: 2.2rem;
    border-bottom: 1px solid var(--snow-line);
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
    border: 1px solid var(--snow-line);
    border-radius: 1.2rem;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.045) 0%, rgba(255, 255, 255, 0.015) 100%), var(--snow-surface);
    box-shadow: var(--snow-shadow);
  }

  .publication-card__image {
    display: block;
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  .publication-card__title {
    margin: 0 0 0.7rem;
    color: var(--snow-text);
    font-size: 1.75rem;
    line-height: 1.26;
  }

  .publication-card__title a {
    color: inherit;
    text-decoration: none;
  }

  .publication-card__title a:hover {
    color: var(--snow-link-hover);
  }

  .publication-card__authors,
  .publication-card__venue {
    margin: 0;
  }

  .publication-card__authors {
    color: var(--snow-text-soft);
    font-size: 1.08rem;
    line-height: 1.65;
  }

  .publication-card__venue {
    margin-top: 0.35rem;
    color: var(--snow-text-muted);
    font-size: 1.05rem;
    line-height: 1.6;
  }

  .publication-card__badges {
    margin: 0.75rem 0 0;
  }

  .publication-card__badge {
    display: inline-block;
    padding: 0.25rem 0.65rem;
    border: 1px solid rgba(214, 161, 95, 0.28);
    border-radius: 0.55rem;
    background: rgba(214, 161, 95, 0.1);
    color: #ffe1b3;
    font-size: 0.92rem;
    font-weight: 700;
  }

  .publication-card__toggle {
    display: none;
  }

  .publication-card__link-row {
    margin-top: 0.9rem;
    color: var(--snow-text-muted);
    font-size: 1rem;
    line-height: 1.7;
  }

  .publication-card__link-row a,
  .publication-card__toggle-label {
    color: var(--snow-link);
    text-decoration: none;
  }

  .publication-card__link-row a:hover,
  .publication-card__toggle-label:hover {
    color: var(--snow-link-hover);
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
    color: var(--snow-text-soft);
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
    color: var(--snow-text-muted);
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

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

<p class="publications-note">* indicates equal contribution. † indicates co-advising. First-author or co-first-author works are highlighted.</p>

{% include base_path %}

{% assign publications_sorted = site.publications | sort: "date" | reverse %}
<div class="publication-filters" aria-label="Publication filters">
  <input id="publication-search" class="publication-filters__input" type="search" placeholder="Search publications...">
  <select id="publication-date" class="publication-filters__select" aria-label="Filter publications by year">
    <option value="">Date</option>
    {% assign seen_year = "" %}
    {% for post in publications_sorted %}
      {% assign post_year = post.date | date: "%Y" %}
      {% unless post_year == seen_year %}
    <option value="{{ post_year }}">{{ post_year }}</option>
        {% assign seen_year = post_year %}
      {% endunless %}
    {% endfor %}
  </select>
  <button id="publication-clear" class="publication-filters__clear" type="button">Clear</button>
</div>

<div class="publication-list">
{% for post in publications_sorted %}
  {% include archive-single-publication-card.html %}
{% endfor %}
</div>

<p id="publication-empty" class="publication-empty">No publications match the current filters.</p>

<script>
  (function () {
    var searchInput = document.getElementById("publication-search");
    var yearSelect = document.getElementById("publication-date");
    var clearButton = document.getElementById("publication-clear");
    var cards = Array.prototype.slice.call(document.querySelectorAll(".publication-list .publication-card"));
    var emptyState = document.getElementById("publication-empty");

    if (!searchInput || !yearSelect || !clearButton || !cards.length) {
      return;
    }

    function normalize(value) {
      return (value || "").toLowerCase().trim();
    }

    function applyFilters() {
      var query = normalize(searchInput.value);
      var year = yearSelect.value;
      var visibleCount = 0;

      cards.forEach(function (card) {
        var haystack = normalize(card.getAttribute("data-search"));
        var cardYear = card.getAttribute("data-year");
        var matchesQuery = !query || haystack.indexOf(query) !== -1;
        var matchesYear = !year || cardYear === year;
        var visible = matchesQuery && matchesYear;

        card.style.display = visible ? "" : "none";
        if (visible) {
          visibleCount += 1;
        }
      });

      emptyState.style.display = visibleCount ? "none" : "block";
    }

    searchInput.addEventListener("input", applyFilters);
    yearSelect.addEventListener("change", applyFilters);
    clearButton.addEventListener("click", function () {
      searchInput.value = "";
      yearSelect.value = "";
      applyFilters();
    });
  })();
</script>
