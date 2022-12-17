---
title: "Cats"
layout: default
excerpt: "Meet Cicero and Figaro."
sitemap: false
permalink: /cats/
---

## Meet Cicero and Figaro

<style>
  .row {
    padding: 8px;
  }
  .col-md-4 {
    padding: 8px;
  }
</style>

<div class="row">
{% for image in site.static_files %}
  {% if image.path contains 'images/cats' %}
  <div class="col-md-4 d-flex align-items-center justify-content-center margin">
  	<a href="{{ site.baseurl }}{{ image.path }}">
  	  <img src="{{ site.baseurl }}{{ image.path }}" alt="image" class="img-fluid">
  	</a>
  </div>
  {% endif %}
{% endfor %}
</div>