---
layout: default
title: Repertoire
description: Selected orchestral, chamber, choral, wind band and musical theatre works conducted by Ben Perche.
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
      A selection of works conducted. Where applicable, the group is listed below each piece with the year the piece was worked on. Pieces listed in chronological order of composer birth date.
    </p>

  {% assign categories = "Orchestral,Chamber,Choral,Opera,Contemporary,Wind Band,Musical Theatre" | split: "," %}
  {% for category in categories %}
    {% include repertoire-category.html category=category %}
  {% endfor %}

  </div>
</section>