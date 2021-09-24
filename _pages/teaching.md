---
layout: page
permalink: /teaching/
title: Teaching
description: 
years: [2016, 2017]
nav: true
---

<div class="publications">
{% for y in site.data.courses.classes%}
  <h2 class="year">{{y.year}}</h2>
  {% for course in y.items%}
  <ol class="bibliography"><li><div class="row">
  <div class="col-sm-2 abbr">
  {% if course.abbr %}
    <abbr class="badge">{{course.abbr}}</abbr>
  {% endif %}
    </div>  
  <div id={{course.id}} class="col-sm-8">
  <div class="title">{{course.name}}</div>
  <div class="author">{{course.inst}}</div>  
  <div class="periodical">
    <u>Role</u>: Teaching Assistant<br>      
    {% if course.hardware %}<em>Hardware used: {{course.hardware}}</em><br>{% endif %}
    {% if course.software %}<em>Software used: {{course.software}}</em><br>{% endif %}
  </div>
    
   <div class="links">  
  {% if course.description %}
      <a class="abstract btn btn-sm z-depth-0" role="button">Description</a>
    {% endif %}
     {% if course.press %}
      <a href="{{ course.press }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Press</a>
    {% endif %}
     {% if course.website %}
      <a href="{{ course.website}}" class="btn btn-sm z-depth-0" role="button" target="_blank">Projects</a>
    {% endif %}
    </div>
    
      {% if course.description %}
    <div class="abstract hidden">
      <p>{{ course.description }}</p>
    </div>
    {% endif %}  
  </div>
    </li>
{% endfor %}
      </ol>
{% endfor %}
</div>
