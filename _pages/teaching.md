---
layout: page
permalink: /teaching/
title: Teaching
years: [2016, 2017, 2018, 2019, 2020, 2021]
description: Materials for courses you taught. Replace this text with your description.
nav: true
---

<div class="teaching">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% courses -f classes -q @*[year={{y}}]* %}
{% endfor %}

</div>

