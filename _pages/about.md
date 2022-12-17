---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About 

{% if site.data.awards %}
<div class="jumbotron">
### Awards
  <ul>
  {% for award in site.data.awards %}
  <li> {{ award.name | replace: "-","&#8211;"}} </li>
  {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.affiliations %}
<div class="jumbotron">
### Affiliations
  <ul>
  {% for affiliation in site.data.affiliations %}
  <li> {{ affiliation.name | replace: "-","&#8211;"}} </li>
  {% endfor %}
  </ul>
</div>
{% endif %}
