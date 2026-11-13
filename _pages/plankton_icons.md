---
layout: page
title: Plankton Icons
permalink: /plankton-icons/
description: 
nav: true
nav_order: 4
---

A visual collection of plankton icons. I drew these while preparing for my PhD defense. All images were created by referencing real, in situ ISIIS imagery. 

Please feel empowered to save and use these icons for all your plankton needs! 

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
</style>
