---
layout: project
project: true
title: EYP Media Works
subtitle: Branding, Logos & Visual Identity
hide_header: true
hide_from_portfolio: true
permalink: /creative/eyp-media-works/
---

<div class="creative-description">

  <p>
    I have been an active member of the European Youth Parliament (EYP) since 2020, participating in over 20
    sessions across various roles including delegate, organiser, media team member, jury member, chairperson, editorial assistant, head organiser and NC board member. My long-term
    involvement has allowed me to deeply engage with EYP’s creative, visual, and communicative aspects.
  </p>

  <p>
    This section highlights my media and branding work created for EYP events. The designs include event logos,
    visual identity concepts, promotional materials, and creative direction elements developed to support
    sessions, workshops, and youth engagement initiatives.
  </p>

  <p>
    Due to privacy and confidentiality considerations, most of my EYP media projects, especially those involving
    identifiable faces or personal information, cannot be showcased publicly. Therefore, the
    works displayed here represent only a small portion of my full creative portfolio.
  </p>


</div>


<a href="https://www.instagram.com/p/C-U09D0tVCJ/" target="_blank" class="video-btn">
  Watch the Published Video Project
</a>


<h2 class="eyp-heading">Logo Designs for Events (2020/2021)</h2>

<!-- AUTO SLIDER -->
<div class="eyp-slider">
  <div class="eyp-slide-track">

    {% for image in site.static_files %}
      {% if image.path contains '/img/creative/eyp-media/logos/' %}
        <div class="eyp-slide">
          <img src="{{ image.path }}" alt="EYP Logo">
        </div>
      {% endif %}
    {% endfor %}

    <!-- duplicate for seamless infinite scroll -->
    {% for image in site.static_files %}
      {% if image.path contains '/img/creative/eyp-media/logos/' %}
        <div class="eyp-slide">
          <img src="{{ image.path }}" alt="EYP Logo">
        </div>
      {% endif %}
    {% endfor %}

  </div>
</div>

<h2 class="eyp-heading">Moodboards (2020-2021)</h2>

<div class="mood-slider">
  <div class="mood-slide-track">

    {% for image in site.static_files %}
      {% if image.path contains '/img/creative/eyp-media/moodboards/' %}
        <div class="mood-slide">
          <img src="{{ image.path }}" alt="Moodboard">
        </div>
      {% endif %}
    {% endfor %}

    <!-- duplicate images for seamless infinite loop -->
    {% for image in site.static_files %}
      {% if image.path contains '/img/creative/eyp-media/moodboards/' %}
        <div class="mood-slide">
          <img src="{{ image.path }}" alt="Moodboard">
        </div>
      {% endif %}
    {% endfor %}

  </div>
</div>
