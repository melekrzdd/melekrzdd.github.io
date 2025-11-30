---
layout: project
project: true
title: Photography
subtitle: Visual Storytelling & Creative Perspectives
hide_header: true
hide_from_portfolio: true
permalink: /creative/photography/
---

<div class="creative-description">
  <p>
    Photography has always been my passion and my love language. Wherever I go, my camera comes with me -capturing moments, places, people, and the quiet details that often go unnoticed. I believe everything carries its own kind of beauty if you’re willing to look at it from a different angle. In this section, you’re invited to see a piece of the world through my eyes. 
  </p>

<p>
    For privacy reasons, images containing identifiable faces or sensitive content have been intentionally omitted.
</p>

</div>

<h2 class="photo-heading"></h2>

<style>
/* ===== COVERFLOW CAROUSEL STYLES ===== */

.coverflow-wrapper {
  width: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  margin: 60px 0 100px 0;
  perspective: 1200px;
}

.coverflow {
  display: flex;
  gap: 20px;
  transition: transform 0.5s ease;
  transform-style: preserve-3d;
}

.coverflow-image {
  width: 280px;
  height: 380px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 8px 30px rgba(0,0,0,0.2);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  cursor: pointer;
}

/* Center image */
.coverflow-image.active {
  transform: scale(1.15) rotateY(0deg) translateZ(120px);
  box-shadow: 0 12px 40px rgba(0,0,0,0.35);
  z-index: 3;
}

/* Left image */
.coverflow-image.left {
  transform: rotateY(40deg) translateZ(40px);
  opacity: 0.85;
  z-index: 2;
}

/* Right image */
.coverflow-image.right {
  transform: rotateY(-40deg) translateZ(40px);
  opacity: 0.85;
  z-index: 2;
}

@media(max-width: 600px) {
  .coverflow-image {
    width: 180px;
    height: 260px;
  }
}
</style>

<!-- ===== CAROUSEL HTML ===== -->
<div class="coverflow-wrapper">
  <div class="coverflow" id="coverflow">
    {% for image in site.static_files %}
      {% if image.path contains '/img/creative/photography/' %}
        <img src="{{ image.path }}" class="coverflow-image" alt="Photography image">
      {% endif %}
    {% endfor %}
  </div>
</div>

<!-- ===== COVERFLOW JS ===== -->
<script>
document.addEventListener("DOMContentLoaded", function () {
  const coverflow = document.getElementById("coverflow");
  const images = Array.from(coverflow.querySelectorAll(".coverflow-image"));

  if (images.length === 0) return;

  let currentIndex = 0;

  function updateCoverflow() {
    const imgWidth = images[0].offsetWidth || 280; // fallback
    const gap = 20; // same as your CSS gap
    const wrapper = coverflow.parentElement;
    const wrapperWidth = wrapper.offsetWidth;

    // reset classes
    images.forEach((img, i) => {
      img.classList.remove("active", "left", "right");

      const prev = (currentIndex - 1 + images.length) % images.length;
      const next = (currentIndex + 1) % images.length;

      if (i === currentIndex) {
        img.classList.add("active");
      } else if (i === prev) {
        img.classList.add("left");
      } else if (i === next) {
        img.classList.add("right");
      }
    });

    // center the active image in the wrapper (this is what makes it loop smoothly)
    const itemWidth = imgWidth + gap;
    const centerOffset = wrapperWidth / 2 - (currentIndex + 0.5) * itemWidth;
    coverflow.style.transform = `translateX(${centerOffset}px)`;
  }

  function next() {
    currentIndex = (currentIndex + 1) % images.length;
    updateCoverflow();
  }

  function prev() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    updateCoverflow();
  }

  // Auto-slide continuously
  let intervalId = setInterval(next, 3000);

  // Pause on hover (optional, but feels nicer on desktop)
  coverflow.addEventListener("mouseenter", () => {
    clearInterval(intervalId);
  });

  coverflow.addEventListener("mouseleave", () => {
    intervalId = setInterval(next, 3000);
  });

  // Swipe events for mobile
  let startX = 0;

  coverflow.addEventListener("touchstart", e => {
    startX = e.touches[0].clientX;
  });

  coverflow.addEventListener("touchend", e => {
    let endX = e.changedTouches[0].clientX;
    if (endX < startX - 50) next();
    if (endX > startX + 50) prev();
  });

  updateCoverflow();
});
</script>
