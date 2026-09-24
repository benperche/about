---
layout: default
title: Contact
description: Contact Ben Perche about conducting, programming, or anything else.
---

<div class="page-header">
  <div class="container">
    <p class="page-header__label">Contact</p>
    <h1>Get in Touch</h1>
  </div>
</div>

<section>
  <div class="container">
    <div class="contact__body">
      <p>
        For conducting enquiries, programming discussions, or general correspondence,
        please reach out by email.
      </p>

      <a href="mailto:{{ site.author.email }}" class="contact__email">{{ site.author.email }}</a>

      {% include social-links.html %}
    </div>
  </div>
</section>
