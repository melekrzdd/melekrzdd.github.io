---
layout: project
project: true
title: CYC Career Fair 2025
subtitle: Media & Design Work
hide_header: true
hide_from_portfolio: true
permalink: /creative/cyc-career-fair-2025/
---

<div class="creative-description">

  <p>
    The “Constructor Your Career” Career Fair 2025, held on March 5th, 2025 at Constructor University Bremen, 
    was the largest career event in the university’s history. Bringing together 45 participating companies and over 
    1,000 students from multiple universities, the fair served as a dynamic platform for professional networking, 
    recruitment, and industry engagement. Leading organizations from technology, engineering, consulting, research, 
    and other sectors participated, giving students direct access to recruiters, internship and full-time job 
    opportunities, and valuable insights into diverse career paths.
  </p>

  <p>
    As the Student Assistant in charge of Marketing, I played a key role in shaping the fair’s visibility and impact. 
    I was responsible for developing and executing comprehensive marketing strategies, which included:
  </p>

  <ul>
    <li>Designing visually compelling promotional materials (posters, banners, social templates, and email assets).</li>
    <li>Coordinating and scheduling social media campaigns across multiple channels to maximize awareness and attendance.</li>
    <li>Targeting communication toward students and prospective attendees to ensure broad engagement.</li>
    <li>Collaborating closely with the Career Services team and external partners to maintain consistent event branding.</li>
  </ul>

  <p>
    Beyond pre-event marketing, I contributed actively on the day of the fair, helping coordinate logistics, supporting company 
    representatives, and ensuring smooth operations for both exhibitors and attendees. My involvement strengthened my leadership, 
    communication, and organizational skills, while contributing to the overall success of a large-scale, high-visibility 
    university event.

  </p>

  <p>

    All the designs below were prepared by me. 

  </p>

</div>

<div class="brochure-cta">

  <a href="/img/creative/cyc-career-fair/Catalogue-Career-Fair-2025-v4.pdf" 
     target="_blank" 
     class="btn-brochure btn-secondary">
    View the Catalogue
  </a>
</div>


<div class="creative-gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/img/creative/cyc-career-fair/' %}
      
      {%- comment -%}
      EXCLUDE the PDF cover image so it doesn't appear huge
      {%- endcomment -%}
      {% unless image.path contains 'cover.png' %}
        <div class="gallery-item">
          <img src="{{ image.path }}" alt="">
        </div>
      {% endunless %}

    {% endif %}
  {% endfor %}
</div>

<!-- Team Section -->
<h2 class="team-heading">Our Team</h2>

<div class="team-row">
  <img src="/img/creative/cyc-career-fair/team/teampic.JPG" alt="Team Photo 1">
  <img src="/img/creative/cyc-career-fair/team/teampic2.JPG" alt="Team Photo 2">
</div>

