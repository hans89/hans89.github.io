---
layout: default
excerpt: "Hai Dang's Codin.vn - Home for babbling with Vietnamese"

---
<div id="index">
  <h3><a href="{{ site.url}}/posts/">Recent Posts</a></h3>
  {% for post in site.posts limit:5 %}
  <article>
    {% if post.link %}
      <h2 class="link-post">
      <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> 
      <a href="{{ post.link }}" target="_blank" title="{{ post.title }}"><i class="fa fa-link"></i></a></h2>
    {% else %}
      <h2><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
    {% endif %}
  </article>
  {% endfor %}
</div><!-- /#index -->