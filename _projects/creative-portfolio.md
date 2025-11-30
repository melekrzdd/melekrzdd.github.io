---
layout: project
project: true
title: Creative Portfolio
subtitle: A curated exhibition of my visual design work
thumbnail: img/portfolio/creative.gif
permalink: /creative-portfolio/
hide_header: true
---


<div class="creative-intro">
  <p>A selection of posters, visuals, branding work, and creative designs I've made.</p>
</div>

<div class="creative-categories">
  <a href="/creative/cyc-career-fair-2025/" class="category-btn">CYC Career Fair</a>
  <a href="/creative/eyp-media-works/" class="category-btn">EYP Media Works</a>
  <a href="/creative/more-marketing/" class="category-btn">More Marketing Works</a>
  <a href="/creative/photography/" class="category-btn">Photography</a>
</div>


<div class="creative-gallery">
  {% for image in site.static_files %}
    {% assign parts = image.path | split: '/' %}

    {%- comment -%}
      Example:
      /img/creative/file.png
      parts = ["", "img", "creative", "file.png"]
      → parts.size == 4 → show

      /img/creative/cyc-career-fair/file.png
      parts = ["", "img", "creative", "cyc-career-fair", "file.png"]
      → parts.size == 5 → hide
    {%- endcomment -%}

    {% if parts[1] == 'img' and parts[2] == 'creative' and parts.size == 4 %}
      <div class="gallery-item">
        <img src="{{ image.path }}" alt="">
      </div>
    {% endif %}
  {% endfor %}
</div>
