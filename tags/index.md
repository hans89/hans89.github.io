---
layout: default
title: Tags
date: 2016-03-06T19:09:39+01:00
excerpt: "Tags"
share: false
---

<div id="index">
  <h1>{{ page.title }}</h1>
  {% if site.tags.size > 0 %}
    <ul class="tag_box inline">
      {% for cat in site.tags %}
        <li><a href="#{{ cat | first }}">{{ cat | first }}<span>{{cat | last | size}}</span></a></li>
      {% endfor %}
    </ul>
    <div class="index">
    {% for cat in site.tags %} 
      <h3 id="{{ cat | first }}">{{ cat | first }}</h3>
      {% for post in cat[1] %}      
        {% include _post-item.html %}
      {% endfor %}
    {% endfor %}
    </div>
  {% else %}
    There is currently no tag available.
  {% endif %}
</div>
