---
layout: default
title: "Archives"
date: 2016-03-05T18:57:04+01:00
modified:
excerpt: "Archives"
---

<div id="index">
  <h1>{{ page.title }}</h1>
  {% capture written_year %}'None'{% endcapture %}
  <!-- This loops through the paginated posts -->
  {% for post in site.posts %}  
    {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if year != written_year %}
      <h3>{{ year }}</h3>
      {% capture written_year %}{{ year }}{% endcapture %}
    {% endif %}
    {% include _post-item.html %}
  {% endfor %}
</div><!-- /#index -->