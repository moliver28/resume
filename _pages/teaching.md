---
layout: page
permalink: /eaching/
title: Teaching
description: 
years: [2016]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% for course in site.data.courses%}
  <div class="row">
  <div class="col-sm-2 abbr">
  {% if course.abbr %}
    <abbr class="badge">{{course.abbr}}</abbr>
  {% endif %}
  </div>
  </div>
  {% endfor %}
{% endfor %}

</div>
