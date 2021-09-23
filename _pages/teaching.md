---
layout: page
permalink: /teaching/
title: Teaching
description: 
years: [2016, 2017]
nav: true
---

<div class="publications">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% for course in site.data.courses.{{y}}%}
  <ol class="bibliography"><li><div class="row">
  <div class="col-sm-2 abbr">
  {% if course.abbr %}
    <abbr class="badge">{{course.abbr}}</abbr>
  {% endif %}
    </div>  
  <div id="ee3712016" class="col-sm-8">
  <div class="title">{{course.name}}</div>
  <div class="author">{{course.inst}}</div>  
  <div class="periodical">
    <u>Role</u>: Teaching Assistant<br>      
    <em>Hardware used: {{course.hardware}}</em><br>
    <em>Software used: {{course.software}}</em><br>
  </div>
    
   <div class="links">  
  {% if course.description %}
      <a class="abstract btn btn-sm z-depth-0" role="button">Description</a>
    {% endif %}  
    </div>
    
      {% if course.description %}
    <div class="abstract hidden">
      <p>{{ course.description }}</p>
    </div>
    {% endif %}  
  </div>
  {% endfor %}
    
    
{% endfor %}

</div>
