---
layout: default
title: Home
---

<div class="hero">
  <div class="container--wide">
    <div class="hero__inner">
      <div class="hero__text">
        <p class="hero__eyebrow">Conductor</p>
        <h1 class="hero__name">Ben Perche</h1>
        <p class="hero__tagline">{{ site.tagline }}</p>
        <div class="hero__links">
          <a href="{{ '/about/' | relative_url }}" class="btn btn--primary">About</a>
          <a href="{{ '/repertoire/' | relative_url }}" class="btn btn--outline">Repertoire</a>
        </div>
      </div>
      <img src="{{ '/assets/images/BenRecital2026.png' | relative_url }}" alt="Ben Perche" class="hero__image">    
    </div>
  </div>
</div>

<!-- Brief intro section -->
<section>
  <div class="container">
    <h2>About</h2>
    <div class="bio__body">
      <p>
        Ben Perche is a new generation Australian conductor with a broad repertoire spanning orchestral, choral, wind band and chamber music, with a particular interest in new music.
      </p>
      <p><a href="{{ '/about/' | relative_url }}">Read full bio →</a></p>
    </div>
  </div>
</section>

<!-- Projects teaser -->
<section>
  <div class="container">
    <h2>Projects</h2>
    <p style="color:var(--mid); margin-bottom:2rem;">Tools and resources I've created for musicians and school music administrators.</p>
    <a href="{{ '/projects/' | relative_url }}" class="btn btn--outline">View projects</a>
  </div>
</section>
