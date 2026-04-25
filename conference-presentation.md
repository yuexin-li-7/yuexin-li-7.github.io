---
layout: page
title: Conference Presentation
permalink: /conference-presentation/
---

<p class="conference-intro">Conference presentation highlights.</p>

<p class="conference-upload-guide">Put all conference photos in <code>/media/conference-presentations/</code> using these filenames:</p>
<ul class="conference-file-list">
  <li><code>cds-2026.jpg</code></li>
  <li><code>nyu-ma-psychology-2026.jpg</code></li>
  <li><code>cns-2025.jpg</code></li>
  <li><code>aps-global-2024.jpg</code></li>
</ul>

{% assign conference_items = "2026 Cognitive Development Society Meeting|cds-2026.jpg,2026 NYU MA Psychology Research Conference|nyu-ma-psychology-2026.jpg,2025 Cognitive Neuroscience Society Meeting|cns-2025.jpg,2024 APS Global Summit|aps-global-2024.jpg" | split: "," %}

<section class="conference-gallery" aria-label="Conference presentation photos">
  {% for item in conference_items %}
    {% assign parts = item | split: "|" %}
    {% assign conference_name = parts[0] | strip %}
    {% assign filename = parts[1] | strip %}
    {% assign image_path = '/media/conference-presentations/' | append: filename %}
    {% assign image_file = site.static_files | where: "path", image_path | first %}

    <article class="conference-card">
      <div class="conference-card-media">
        {% if image_file %}
          <img src="{{ image_path | relative_url }}" alt="{{ conference_name }}" loading="lazy" decoding="async">
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
