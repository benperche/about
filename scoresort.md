---
layout: default
title: ScoreSort
description: A macOS app for working with music PDFs — combine, rename, split, and rotate parts.
---

<div class="page-header">
  <div class="container">
    <p class="page-header__label">macOS App</p>
    <h1>ScoreSort</h1>
  </div>
</div>

<section>
  <div class="container--wide">
    <div class="scoresort__intro">
      <p class="scoresort__tagline">All your music PDF work in one place.</p>
      <p>
        ScoreSort is a macOS app for musicians and ensemble directors who work with PDF parts.
        Combine separate parts into a single print-ready file, rename a folder of scans, put
        files into score order, split a bound scan apart, or fix rotated pages — without leaving
        the app.
      </p>
      <p>
        It runs entirely on your device. No accounts, no internet, no tracking —
        just your files.
      </p>
      <div class="scoresort__actions">
        <a href="/assets/downloads/ScoreSort-1.0.dmg" class="btn btn--primary">Download for Mac</a>
        <a href="https://ko-fi.com/YOUR_USERNAME" class="btn btn--outline" target="_blank" rel="noopener">Pay what you want →</a>
      </div>
      <p class="scoresort__req">Requires macOS 13 Ventura or later &nbsp;·&nbsp; Apple Silicon &amp; Intel</p>
    </div>
  </div>
</section>

<section class="scoresort__carousel-section">
  <div class="container--wide">

    <div class="carousel" id="scoresort-carousel">
      <div class="carousel__track">

        <div class="carousel__slide">
          <img src="{{ '/assets/images/scoresort/01 combiner.png' | relative_url }}" alt="Combine PDFs tab" class="carousel__img">
          <div class="carousel__caption">
            <h3>Combine PDFs</h3>
            <p>Drag in separate instrument parts and merge them into a single print-ready PDF. Save your usual instrument allocations as Ensemble Presets, and use Collate to interleave pages so each player's copies print together.</p>
          </div>
        </div>

        <div class="carousel__slide">
          <img src="{{ '/assets/images/scoresort/02 renamer.png' | relative_url }}" alt="Rename Files tab" class="carousel__img">
          <div class="carousel__caption">
            <h3>Rename Files</h3>
            <p>Replace the filenames of a whole folder at once — ideal for parts downloaded from IMSLP. Enter a base name, fill in each instrument, and the app previews the top corner of every file so you can confirm what you're naming.</p>
          </div>
        </div>

        <div class="carousel__slide">
          <img src="{{ '/assets/images/scoresort/03 score order.png' | relative_url }}" alt="Score Order Sorter" class="carousel__img">
          <div class="carousel__caption">
            <h3>Score Order</h3>
            <p>Add score-order prefixes to already-named files in seconds. Drag a folder in, tweak the order if needed, and re-number everything in one step. Your preferred instrument order is saved in Preferences.</p>
          </div>
        </div>

        <div class="carousel__slide">
          <img src="{{ '/assets/images/scoresort/04 splitter.png' | relative_url }}" alt="Split PDF tab" class="carousel__img">
          <div class="carousel__caption">
            <h3>Split PDF</h3>
            <p>Turn a single bound scan into individual parts. Navigate pages with the arrow keys, place split markers with Space, then name each output file — with score-order prefixes added automatically if you want them.</p>
          </div>
        </div>

        <div class="carousel__slide">
          <img src="{{ '/assets/images/scoresort/05 rotator.png' | relative_url }}" alt="Rotate Pages tab" class="carousel__img">
          <div class="carousel__caption">
            <h3>Rotate Pages</h3>
            <p>Fix sideways or upside-down pages from your scans. Rotate a single page, all pages, or all odd/even pages at once — handy for landscape-scanned scores where every other page came out inverted.</p>
          </div>
        </div>

      </div>

      <button class="carousel__btn carousel__btn--prev" aria-label="Previous">&#8249;</button>
      <button class="carousel__btn carousel__btn--next" aria-label="Next">&#8250;</button>

      <div class="carousel__dots">
        <button class="carousel__dot active" aria-label="Slide 1"></button>
        <button class="carousel__dot" aria-label="Slide 2"></button>
        <button class="carousel__dot" aria-label="Slide 3"></button>
        <button class="carousel__dot" aria-label="Slide 4"></button>
        <button class="carousel__dot" aria-label="Slide 5"></button>
      </div>
    </div>

  </div>
</section>

<section>
  <div class="container--wide">
    <div class="scoresort__pwyw">
      <div class="scoresort__pwyw-text">
        <h2>Pay what you want</h2>
        <p>
          ScoreSort is a niche tool made for a small community. There's no price tag —
          download it free and pay whatever feels right if it saves you time.
          Every contribution helps fund continued development.
        </p>
        <a href="https://ko-fi.com/YOUR_USERNAME" class="btn btn--primary" target="_blank" rel="noopener">Support on Ko-fi</a>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container--wide">
    <h2>Installing ScoreSort</h2>
    <ol class="scoresort__install-steps">
      <li>Download the <code>.dmg</code> file above.</li>
      <li>Open the <code>.dmg</code> and drag <strong>ScoreSort</strong> into your <strong>Applications</strong> folder.</li>
      <li>Open ScoreSort from your Applications folder.</li>
    </ol>
    <p class="scoresort__privacy-note">
      ScoreSort is notarized by Apple. It has no network access and touches only the files you
      explicitly open. Read the <a href="/scoresort-privacy/">privacy policy</a> for full details.
    </p>
  </div>
</section>

<script>
(function () {
  const carousel = document.getElementById('scoresort-carousel');
  if (!carousel) return;

  const slides = carousel.querySelectorAll('.carousel__slide');
  const dots   = carousel.querySelectorAll('.carousel__dot');
  let current  = 0;

  function goTo(n) {
    slides[current].classList.remove('active');
    dots[current].classList.remove('active');
    current = (n + slides.length) % slides.length;
    slides[current].classList.add('active');
    dots[current].classList.add('active');
  }

  slides[0].classList.add('active');

  carousel.querySelector('.carousel__btn--prev').addEventListener('click', () => goTo(current - 1));
  carousel.querySelector('.carousel__btn--next').addEventListener('click', () => goTo(current + 1));
  dots.forEach((dot, i) => dot.addEventListener('click', () => goTo(i)));
})();
</script>
