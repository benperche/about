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

    {% assign categories = site.data.repertoire | map: "category" | uniq | sort %}

    {% for category in categories %}
    <div class="repertoire__category">
      <h3 class="repertoire__category-title">{{ category }}</h3>
      <ul class="repertoire__list">
        {% assign works = site.data.repertoire | where: "category", category | sort: "composer" %}
        {% for work in works %}
        <li class="repertoire__item">
          <span class="repertoire__composer">{{ work.composer }}</span>
          <span class="repertoire__work">{{ work.work }}</span>
        </li>
        {% endfor %}
      </ul>
    </div>
    {% endfor %}

  </div>
</section>
