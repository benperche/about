---
layout: default
title: Repertoire
---

<div class="page-header">
  <div class="container">
    <p class="page-header__label">Repertoire</p>
    <h1>Selected Works</h1>
  </div>
</div>

<section>
  <div class="container">
    <p class="repertoire__intro">
      A selection of works conducted.
    </p>

  {% assign main_categories = "Orchestral,Chamber,Choral,Opera,Contemporary" | split: "," %}
  {% assign band_categories = "Wind Band" | split: "," %}
  {% assign theatre_categories = "Musical Theatre" | split: "," %}

  <h2 class="repertoire__section-title">Orchestral &amp; Chamber Works</h2>
  {% for category in main_categories %}
    {% assign works = site.data.repertoire | where: "category", category | sort: "birth_year" %}
    {% if works.size > 0 %}
    <div class="repertoire__category">
      <h3 class="repertoire__category-title">{{ category }}</h3>
      <ul class="repertoire__list">
        {% for work in works %}
        <li class="repertoire__item">
          <div class="repertoire__main">
            <span class="repertoire__composer">{{ work.composer }}</span>
            <span class="repertoire__work">{{ work.work }}</span>
          </div>
          {% if work.group %}<span class="repertoire__group">{{ work.group }}</span>{% endif %}
          {% if work.last_conducted %}<span class="repertoire__year">{{ work.last_conducted }}</span>{% endif %}
        </li>
        {% endfor %}
      </ul>
    </div>
    {% endif %}
  {% endfor %}

  <h2 class="repertoire__section-title">Wind Band</h2>
  {% for category in band_categories %}
    {% assign works = site.data.repertoire | where: "category", category | sort: "birth_year" %}
    {% if works.size > 0 %}
    <div class="repertoire__category">
      <h3 class="repertoire__category-title">{{ category }}</h3>
      <ul class="repertoire__list">
        {% for work in works %}
        <li class="repertoire__item">
          <div class="repertoire__main">
            <span class="repertoire__composer">{{ work.composer }}</span>
            <span class="repertoire__work">{{ work.work }}</span>
          </div>
          {% if work.group %}<span class="repertoire__group">{{ work.group }}</span>{% endif %}
          {% if work.last_conducted %}<span class="repertoire__year">{{ work.last_conducted }}</span>{% endif %}
        </li>
        {% endfor %}
      </ul>
    </div>
    {% endif %}
  {% endfor %}

  <h2 class="repertoire__section-title">Musical Theatre</h2>
    {% for category in theatre_categories %}
      {% assign works = site.data.repertoire | where: "category", category | sort: "birth_year" %}
      {% if works.size > 0 %}
      <div class="repertoire__category">
      <h3 class="repertoire__category-title">{{ category }}</h3>
      <ul class="repertoire__list">
        {% for work in works %}
        <li class="repertoire__item">
          <div class="repertoire__main">
            <span class="repertoire__composer">{{ work.composer }}</span>
            <span class="repertoire__work">{{ work.work }}</span>
          </div>
          {% if work.group %}<span class="repertoire__group">{{ work.group }}</span>{% endif %}
          {% if work.last_conducted %}<span class="repertoire__year">{{ work.last_conducted }}</span>{% endif %}
        </li>
        {% endfor %}
      </ul>
    </div>
          {% endfor %}
        </ul>
      </div>
      {% endif %}
    {% endfor %}

  </div>
</section>