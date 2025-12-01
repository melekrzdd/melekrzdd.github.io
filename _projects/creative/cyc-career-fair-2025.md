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
    The “Construct Your Career” Career Fair 2025, held on March 5th, 2025 at Constructor University Bremen, 
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

<!-- Posters gallery -->
<div class="creative-gallery">
  {% assign fair_images = site.static_files | sort: "path" %}

  {%- comment -%}
    Convert to array of only the allowed images
  {%- endcomment -%}
  {% assign posters = "" | split: "" %}
  {% for image in fair_images %}
    {% assign parts = image.path | split: "/" %}
    {% if parts[3] == "cyc-career-fair" and parts.size == 5 %}
      {% assign posters = posters | push: image %}
    {% endif %}
  {% endfor %}

  {%- comment -%}
    Shuffle the posters (Liquid hack: sort by random key)
  {%- endcomment -%}
  {% assign shuffled = posters | sort: "modified_time" %}

  {% for image in shuffled %}
    <div class="gallery-item">
      <img src="{{ image.path }}" alt="">
    </div>
  {% endfor %}
</div>


<!-- Team Section -->
<section id="team-section" class="team-section">
  <h2 class="team-heading">Our Team</h2>

  <div class="team-row">
    <img src="/img/creative/cyc-career-fair/team/teampic.JPG" alt="Team Photo 1">
    <img src="/img/creative/cyc-career-fair/team/teampic2.JPG" alt="Team Photo 2">
  </div>
</section>

<style>
  /* ---- Layout fix JUST for this page ---- */

  /* override any column layout from the theme */
  .cyc-gallery {
    column-count: unset !important;
    column-gap: 0 !important;
    -webkit-column-count: unset !important;
    -webkit-column-gap: 0 !important;
    -moz-column-count: unset !important;
    -moz-column-gap: 0 !important;

    display: flex !important;
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;
    margin-top: 40px;
  }

  .cyc-gallery .gallery-item {
    flex: 1 1 calc(50% - 30px);
    max-width: 520px;
  }

  .cyc-gallery .gallery-item img {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
  }

  @media (max-width: 768px) {
    .cyc-gallery .gallery-item {
      flex: 1 1 100%;
      max-width: 100%;
    }
  }

  /* team section spacing */
  .team-section {
    margin-top: 80px;
    padding-top: 40px;
  }

  .team-heading {
    text-align: center;
    font-size: 32px;
    margin-bottom: 30px;
  }

 .team-row {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 40px;
  flex-wrap: nowrap; /* ensures side-by-side */
  margin-top: 30px;
}

.team-row img {
  width: 45%;
  max-width: 550px;
  border-radius: 15px;
  box-shadow: 0 6px 20px rgba(0,0,0,0.15);
}

</style>
