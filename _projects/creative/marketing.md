---
layout: project
project: true
title: More Marketing Works
subtitle: Designs for Campus-Wide Events & Initiatives
hide_header: true
hide_from_portfolio: true
permalink: /creative/more-marketing/
---

<!-- DESCRIPTION -->
<div class="creative-description">

  <p>
    This section showcases a collection of marketing and design works I created for various campus-wide events, clubs, and 
    initiatives at Constructor University. Throughout my involvement in different student organizations and project teams, 
    I contributed to the visual identity, branding, and promotional materials of numerous activities across the university.
  </p>



</div>

<!-- AUTO GALLERY -->
<div class="creative-gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/img/creative/more-marketing/' %}
      <div class="gallery-item">
        <img src="{{ image.path }}" alt="Marketing Work by Melek Rzazade">
      </div>
    {% endif %}
  {% endfor %}
</div>
