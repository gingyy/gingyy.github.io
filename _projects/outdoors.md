---
layout: page
title: Hiking & cycling
description: 
img: assets/img/h_allgaeu.jpeg
importance: 2
category: 
---


<!-- The grid container initialized for Masonry -->
<div class="row grid masonry">
    <!-- Item 1: Horizontal Image -->
    <div class="grid-item col-sm-6 col-md-4 mb-4">
        <a href="{{ '/assets/img/h_allgaeu.jpeg' | relative_url }}" class="lightbox-link">
            {% include figure.liquid loading="eager" path="assets/img/h_allgaeu.jpg" title="Click to zoom horizontal view" class="img-fluid rounded z-depth-1" %}
        </a>
        <div class="caption mt-2 text-muted small">Testing.</div>
    </div>
    <!-- Item 2: Vertical Image (Fits perfectly under or next to others) -->
    <div class="grid-item col-sm-6 col-md-4 mb-4">
        <a href="{{ '/assets/img/h_blue.jpeg' | relative_url }}" class="lightbox-link">
            {% include figure.liquid loading="eager" path="assets/img/h_blue.jpeg" title="Click to zoom portrait view" class="img-fluid rounded z-depth-1" %}
        </a>
        <div class="caption mt-2 text-muted small">Testing.</div>
    </div>
    <!-- Item 3: Another Vertical Image -->
    <div class="grid-item col-sm-6 col-md-4 mb-4">
        <a href="{{ '/assets/img/h_cow.jpeg' | relative_url }}" class="lightbox-link">
            {% include figure.liquid loading="eager" path="assets/img/h_cow.jpeg" title="Click to zoom portrait view" class="img-fluid rounded z-depth-1" %}
        </a>
        <div class="caption mt-2 text-muted small">Testing.</div>
    </div>
    <!-- Item 4: Square Image -->
    <div class="grid-item col-sm-6 col-md-4 mb-4">
        <a href="{{ '/assets/img/h_ebenalp.jpeg' | relative_url }}" class="lightbox-link">
            {% include figure.liquid loading="eager" path="assets/img/h_ebenalp.jpeg" title="Click to zoom square view" class="img-fluid rounded z-depth-1" %}
        </a>
        <div class="caption mt-2 text-muted small">Testing.</div>
    </div>
</div>






<script>
    // Initialize Pinterest-style Masonry layout
    $(document).ready(function() {
        var $grid = $('.masonry').imagesLoaded(function() {
            $grid.masonry({
                itemSelector: '.grid-item',
                percentPosition: true
            });
        });

        // Initialize Zoom Lightbox Grouping
        $('.masonry').magnificPopup({
            delegate: '.lightbox-link', 
            type: 'image',
            gallery: {
                enabled: true // Allows users to click arrow keys to cycle through all images
            },
            image: {
                titleSrc: function(item) {
                    // Pulls the text from the caption div right beneath the image to show inside the lightbox zoom view
                    return item.el.parent().find('.caption').text();
                }
            },
            mainClass: 'mfp-with-zoom', 
            zoom: {
                enabled: true,
                duration: 300, // Smooth 0.3s expand animation
                easing: 'ease-in-out'
            }
        });
    });
</script>
