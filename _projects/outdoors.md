---
layout: page
title: Hiking & cycling
description: 
img: assets/img/h_oesch.jpeg
importance: 2
category: 
---

<ins>[back](https://gingyy.github.io/other)</ins>
<br><br>
mountains <3

<div class="photo-gallery">
  {% assign photos = 
    "assets/img/h_hoernlihuette.jpeg|Hörnliweg, Switzerland;
    assets/img/h_allgaeu.jpeg|Allgäu, Germany;
    assets/img/h_yos.jpeg|Yosemite, California;

    assets/img/h_cow.jpeg|Schwarzwald, Germany;
    assets/img/h_matterhorn_vert.jpeg|Matterhorn, Switzerland;
    assets/img/h_glacier_vert.jpeg|Gornergletscher, Switzerland; 

    assets/img/h_bike_1.jpeg|Golden Gate Bridge, California;
    assets/img/h_hh.jpeg|Hawk Hill, California;
    assets/img/h_group.jpeg|Marin County, California;

    assets/img/h_ridge.jpeg|Herzogstand & Heimgarten, Germany;
    assets/img/h_tegelberg.jpeg|Tegelberg, Germany;
    assets/img/h_hk.jpeg|Maclehose Trail, Hong Kong;

    assets/img/h_dv.jpeg|Death Valley, California;
    assets/img/h_poland.jpeg|High Tatras, Poland;   
    assets/img/h_ut_vert.jpeg|Capitol Reef, Utah;

    assets/img/h_partnachklamm.jpeg|Partnachklamm, Germany;
    assets/img/h_watzmann.jpeg|Watzmann, Germany; 
    assets/img/h_oesch.jpeg|Oeschinensee, Switzerland" | split: ";" %}





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
