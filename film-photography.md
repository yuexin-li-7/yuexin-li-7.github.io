---
layout: page
title: Film Photography
permalink: /film-photography/
---

{% assign kodak_gold_frames = "01,02,04,05,06,07,08,09,10,11,12,13" | split: "," %}
<section class="film-roll">
  <h2 class="film-roll-title">Kodak Gold 200</h2>
  <div class="film-grid">
    {% for frame in kodak_gold_frames %}
      <figure class="film-frame">
        <button class="film-thumb-button" type="button" aria-label="Open Kodak Gold 200 frame {{ frame }}">
          <img src="{{ '/media/film-photography/thumbnails/kodak-gold-200/frame-' | append: frame | append: '.jpg' | relative_url }}" data-full="{{ '/media/film-photography/kodak-gold-200/frame-' | append: frame | append: '.jpeg' | relative_url }}" alt="Kodak Gold 200 frame {{ frame }}" loading="lazy" decoding="async" fetchpriority="low">
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

{% assign kodak_ultramax_frames = "01,02,03,04,05,06,07,08,09,10,11,12,13,14,15,16" | split: "," %}
<section class="film-roll">
  <h2 class="film-roll-title">Kodak Ultramax 400</h2>
  <div class="film-grid">
    {% for frame in kodak_ultramax_frames %}
      <figure class="film-frame">
        <button class="film-thumb-button" type="button" aria-label="Open Kodak Ultramax 400 frame {{ frame }}">
          <img src="{{ '/media/film-photography/thumbnails/kodak-ultramax-400/frame-' | append: frame | append: '.jpg' | relative_url }}" data-full="{{ '/media/film-photography/kodak-ultramax-400/frame-' | append: frame | append: '.JPG' | relative_url }}" alt="Kodak Ultramax 400 frame {{ frame }}" loading="lazy" decoding="async" fetchpriority="low">
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

{% assign kodak_colorplus_frames = "01,02,03,04" | split: "," %}
<section class="film-roll">
  <h2 class="film-roll-title">Kodak ColorPlus 200</h2>
  <div class="film-grid">
    {% for frame in kodak_colorplus_frames %}
      <figure class="film-frame">
        <button class="film-thumb-button" type="button" aria-label="Open Kodak ColorPlus 200 frame {{ frame }}">
          <img src="{{ '/media/film-photography/thumbnails/kodak-colorplus-200/frame-' | append: frame | append: '.jpg' | relative_url }}" data-full="{{ '/media/film-photography/kodak-colorplus-200/frame-' | append: frame | append: '.JPG' | relative_url }}" alt="Kodak ColorPlus 200 frame {{ frame }}" loading="lazy" decoding="async" fetchpriority="low">
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

{% assign quick_snap_frames = "01,02,03,04,05,06,07,08" | split: "," %}
<section class="film-roll">
  <h2 class="film-roll-title">Fuji film 400 Quick Snap</h2>
  <div class="film-grid">
    {% for frame in quick_snap_frames %}
      <figure class="film-frame">
        <button class="film-thumb-button" type="button" aria-label="Open Fuji film 400 Quick Snap frame {{ frame }}">
          <img src="{{ '/media/film-photography/thumbnails/fujifilm-400-QuickSnap/frame-' | append: frame | append: '.jpg' | relative_url }}" data-full="{{ '/media/film-photography/fujifilm-400-QuickSnap/frame-' | append: frame | append: '.JPG' | relative_url }}" alt="Fuji film 400 Quick Snap frame {{ frame }}" loading="lazy" decoding="async" fetchpriority="low">
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

{% assign quick_snap_2_frames = "01,02,03,04,05,06,07,08,09,10,11,12" | split: "," %}
<section class="film-roll">
  <h2 class="film-roll-title">Fuji film 400 Quick Snap 2</h2>
  <div class="film-grid">
    {% for frame in quick_snap_2_frames %}
      <figure class="film-frame">
        <button class="film-thumb-button" type="button" aria-label="Open Fuji film 400 Quick Snap 2 frame {{ frame }}">
          <img src="{{ '/media/film-photography/thumbnails/fujifilm-400-QuickSnap-2/frame-' | append: frame | append: '.jpg' | relative_url }}" data-full="{{ '/media/film-photography/fujifilm-400-QuickSnap-2/frame-' | append: frame | append: '.JPG' | relative_url }}" alt="Fuji film 400 Quick Snap 2 frame {{ frame }}" loading="lazy" decoding="async" fetchpriority="low">
        </button>
      </figure>
    {% endfor %}
  </div>
</section>

<div class="film-lightbox" id="film-lightbox" hidden role="dialog" aria-modal="true" aria-label="Enlarged film photograph">
  <button class="film-lightbox-close" id="film-lightbox-close" type="button" aria-label="Close enlarged image">&times;</button>
  <figure class="film-lightbox-figure">
    <img id="film-lightbox-image" src="" alt="">
  </figure>
</div>

<script>
(() => {
  const lightbox = document.getElementById("film-lightbox");
  const lightboxImage = document.getElementById("film-lightbox-image");
  const closeButton = document.getElementById("film-lightbox-close");
  const buttons = document.querySelectorAll(".film-thumb-button");

  if (!lightbox || !lightboxImage || !closeButton || buttons.length === 0) {
    return;
  }

  const closeLightbox = () => {
    lightbox.hidden = true;
    lightboxImage.src = "";
    lightboxImage.alt = "";
    document.body.classList.remove("film-lightbox-open");
  };

  const openLightbox = (thumbnail) => {
    lightboxImage.src = thumbnail.dataset.full || thumbnail.currentSrc || thumbnail.src;
    lightboxImage.alt = thumbnail.alt;
    lightbox.hidden = false;
    document.body.classList.add("film-lightbox-open");
    closeButton.focus();
  };

  buttons.forEach((button) => {
    button.addEventListener("click", () => {
      const thumbnail = button.querySelector("img");
      if (thumbnail) {
        openLightbox(thumbnail);
      }
    });
  });

  closeButton.addEventListener("click", closeLightbox);
  lightbox.addEventListener("click", (event) => {
    if (event.target === lightbox) {
      closeLightbox();
    }
  });

  document.addEventListener("keydown", (event) => {
    if (!lightbox.hidden && event.key === "Escape") {
      closeLightbox();
    }
  });
})();
</script>
