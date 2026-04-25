---
layout: page
title: Conference Presentation
permalink: /conference-presentation/
---

<p class="conference-intro">Conference presentation highlights.</p>
<p class="conference-help">click pictures for specific project page!</p>

{% assign conference_items = "2026 NYU MA Psychology Research Conference|2026-nyu-ma.JPG,2026 Cognitive Development Society Meeting|2026-cds.jpg,2026 Cognitive Development Society Meeting|2026-cds-2.jpg,2025 Columbia AI Summit|2025-ai-summit.JPG,2025 Cognitive Neuroscience Society Meeting|2025-cns.JPG,2024 APS Annual Convention|2024-aps.jpg" | split: "," %}

<section class="conference-gallery" aria-label="Conference presentation photos">
  {% for item in conference_items %}
    {% assign parts = item | split: "|" %}
    {% assign conference_name = parts[0] | strip %}
    {% assign filename = parts[1] | strip %}
    {% assign image_path = '/media/conference-presentations/' | append: filename %}
    {% assign image_file = site.static_files | where: "path", image_path | first %}
    {% assign top_crop = filename contains '2026-cds' %}

    <article class="conference-card">
      <div class="conference-card-media">
        {% if image_file %}
          <img class="conference-card-image{% if top_crop %} conference-card-image-top{% endif %}" src="{{ image_path | relative_url }}" alt="{{ conference_name }}" loading="lazy" decoding="async">
        {% else %}
          <div class="conference-placeholder">
            Add <code>{{ filename }}</code> to <code>/media/conference-presentations/</code>
          </div>
        {% endif %}
      </div>
      <p class="conference-card-caption">{{ conference_name }}</p>
    </article>
  {% endfor %}
</section>
