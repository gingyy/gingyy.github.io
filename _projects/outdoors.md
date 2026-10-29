---
layout: page
title: Hiking & cycling
description: 
img: assets/img/h_allgaeu.jpeg
importance: 2
category: 
---

<ins>[back](https://gingyy.github.io/other)</ins>

<div class="photo-gallery">
  {% assign photos = 
    "assets/img/h_allgaeu.jpeg|Allgäu,
     assets/img/h_blue.jpeg|Blue,
     assets/img/h_cow.jpeg|Countryside,
     assets/img/h_ebenalp.jpeg|Ebenalp" | split: "," %}

  {% for photo in photos %}
    {% assign details = photo | split: "|" %}
    {% assign filename = details[0] | strip %}
    {% assign caption = details[1] | strip %}
    <div class="gallery-item">
      <a
        href="{{ '/assets/img/' | append: filename | relative_url }}"
        class="lightbox-link"
        aria-label="View {{ caption }}"
      >
        {% include figure.liquid
          loading="lazy"
          path=filename
          class="gallery-image"
          title=caption
        %}
      </a>

      <div class="gallery-caption">{{ caption }}</div>
    </div>
  {% endfor %}

</div>

<style>
    .photo-gallery {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    align-items: start;
    gap: 28px 22px;
    margin: 2rem 0;
    }

    .gallery-item {
    min-width: 0;
    }

    .photo-gallery .gallery-item a {
    display: block;
    overflow: hidden;
    border-radius: 12px;
    background: #f3f3f3;
    box-shadow: 0 3px 12px rgba(0, 0, 0, 0.07);
    }

    .photo-gallery .gallery-item img {
    display: block;
    width: 100%;
    height: auto;
    object-fit: contain;
    border-radius: 12px;
    margin: 0;
    transition: transform 0.35s ease;
    }

    .photo-gallery .gallery-item a:hover img {
    transform: scale(1.03);
    }

    .gallery-caption {
    padding: 10px 3px 0;
    font-size: 0.9rem;
    color: var(--global-text-color, #555);
    letter-spacing: 0.02em;
    }

    @media (max-width: 991px) {
    .photo-gallery {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 22px 16px;
    }
    }

    @media (max-width: 575px) {
    .photo-gallery {
        grid-template-columns: 1fr;
        gap: 24px;
    }
    }
</style>

<script>
  $(document).ready(function () {
    $('.photo-gallery').magnificPopup({
      delegate: '.lightbox-link',
      type: 'image',
      gallery: {
        enabled: true
      },
      image: {
        titleSrc: function (item) {
          return item.el
            .closest('.gallery-item')
            .find('.gallery-caption')
            .text();
        }
      },
      mainClass: 'mfp-with-zoom',
      zoom: {
        enabled: true,
        duration: 300,
        easing: 'ease-in-out'
      }
    });
  });
</script>
