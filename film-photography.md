---
layout: page
title: Film Photography
permalink: /film-photography/
---

{% assign kodak_gold_200_frames = site.static_files
  | where_exp: "file", "file.path contains '/media/film-photography/kodak-gold-200/'"
  | where_exp: "file", "file.extname == '.jpeg' or file.extname == '.jpg' or file.extname == '.png'"
  | sort: "path" %}

<section class="film-roll">
  <h2 class="film-roll-title">Kodak Gold 200</h2>
  <div class="film-grid">
    {% for frame in kodak_gold_200_frames %}
      <figure class="film-frame">
        <img src="{{ frame.path | relative_url }}" alt="Kodak Gold 200 frame {{ forloop.index }}">
      </figure>
    {% endfor %}
  </div>
</section>
