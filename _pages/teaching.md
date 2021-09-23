---
layout: page
permalink: /teaching/
title: Teaching
description: 
years: [2016]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% for course in site.data.courses%}
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
    <em> Role: Teaching Assistant</em>      
        <em>Technology/Tools used: {{course.tools}}</em>
  </div>
    
   <div class="links">  
  {% if course.description %}
      <a class="abstract btn btn-sm z-depth-0" role="button">Abstract</a>
    {% endif %}  
    </div>
    
      {% if course.description %}
    <div class="abstract hidden">
      <p>{{ course.descrtiption }}</p>
    </div>
    {% endif %}  
       
  </div>
  </div>
    </li>
  {% endfor %}
{% endfor %}

</div>
