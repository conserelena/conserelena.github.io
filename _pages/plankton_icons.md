---
layout: page
title: Plankton Icons
permalink: /plankton-icons/
description: 
nav: true
nav_order: 4
---

A visual collection of plankton icons. I drew these while preparing for my PhD defense. All images were created by referencing real, in situ ISIIS imagery. 

Please feel empowered to save and use these icons for all your planktonic needs! 

NOTE: If you are viewing this website with a **light** theme, you may not be able to view the icons! 

<div class="plankton-icons-grid">
  {% for icon in site.data.plankton_icons %}
    <figure class="plankton-icon-card">
      <div class="plankton-icon-card__image">
        <img
          src="{{ icon.file | prepend: '/assets/img/plankton_icons/' | relative_url }}"
          alt="{{ icon.name }}"
          loading="lazy"
        >
      </div>
      <figcaption>{{ icon.name }}</figcaption>
    </figure>
  {% endfor %}
</div>


<!-- Download All Plankton Icons -->
<div class="plankton-icons-download">
  <a
    href="{{ '/assets/img/plankton_icons.zip' | relative_url }}"
    download="plankton_icons.zip"
    class="plankton-download-button"
  >
    Download All Icons (.zip)
  </a>
</div>


<style>
  .plankton-icons-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .plankton-icon-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0;
    padding: 0.75rem;
    overflow: hidden;
    background-color: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    transition: transform 0.2s ease;
  }

  .plankton-icon-card:hover {
    transform: translateY(-2px);
  }

  .plankton-icon-card__image {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 120px;
  }

  .plankton-icon-card__image img {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
  }

  .plankton-icon-card figcaption {
    margin-top: 0.5rem;
    font-size: 0.85rem;
    line-height: 1.2;
    color: var(--global-text-color-light);
    text-align: center;
  }


/* Plankton PowerPoint Background */

.plankton-background-section {
  margin-top: 3.5rem;
  padding-top: 2rem;
  border-top: 1px solid var(--global-divider-color);
}

.plankton-background-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem;
  margin-top: 1.5rem;
  background-color: var(--global-card-bg-color);
  border: 1px solid var(--global-divider-color);
  border-radius: 8px;
}

.plankton-background-card img {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 4px;
}

.plankton-background-download {
  display: inline-block;
  padding: 0.6rem 1.2rem;
  border: 1px solid var(--global-theme-color);
  border-radius: 6px;
  color: var(--global-theme-color);
  text-decoration: none;
  font-weight: 500;
}

.plankton-background-download:hover {
  background-color: var(--global-theme-color);
  color: var(--global-bg-color);
  text-decoration: none;
}


/* Download All Icons Button */

.plankton-icons-download {
  display: flex;
  justify-content: center;
  margin-top: 2rem;
  margin-bottom: 1rem;
}

.plankton-download-button {
  display: inline-block;
  padding: 0.7rem 1.5rem;
  border: 1px solid var(--global-theme-color);
  border-radius: 6px;
  color: var(--global-theme-color);
  font-weight: 500;
  text-decoration: none;
}

.plankton-download-button:hover {
  background-color: var(--global-theme-color);
  color: var(--global-bg-color);
  text-decoration: none;
}


</style>



<!-- Plankton PowerPoint Background -->
<section class="plankton-background-section">
  <h2>Plankton PowerPoint Background</h2>

  <p>
    I also created this plankton-themed background for PowerPoint
    presentations, and I used it in my PhD defense presentation. Feel free to download and use it!
  </p>

  <div class="plankton-background-card">
    <img
      src="{{ '/assets/img/plankton_background.png' | relative_url }}"
      alt="Plankton-themed PowerPoint background"
      loading="lazy"
    >

    <a
      href="{{ '/assets/img/plankton_background.png' | relative_url }}"
      download="plankton_background.png"
      class="plankton-background-download"
    >
      Download background
    </a>
  </div>
</section>

