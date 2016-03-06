---
layout: default
title: Categories
date: 2016-03-06T19:09:33+01:00
excerpt: "Catergories"
share: false
---

<div id="index">
  <h1>{{ page.title }}</h1>
  {% if site.categories.size > 0 %}
    <ul class="tag_box">
      {% for cat in site.categories %}
        <li><a href="#{{ cat | first }}">{{ cat | first }}<span>{{cat | last | size}}</span></a></li>
      {% endfor %}
    </ul>
    <div class="index">
    {% for cat in site.categories %} 
      <h3 id="{{ cat | first }}">{{ cat | first }}</h3>
      {% for post in cat[1] %}      
        {% include _post-item.html %}
      {% endfor %}
    {% endfor %}
    </div>
  {% else %}
    There is currently no category available.
  {% endif %}
</div>

