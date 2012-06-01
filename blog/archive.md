---
layout: page
sitemap:
  priority: 1.0
  changefreq: weekly
  lastmod: 2012-05-20T11:37:42-06:00
title: Archive
---

{% for category in site.categories %} 
<h2 id="{{ category[0] }}-ref">{{ category[0] }}</h2>
<ul>
  {% for post in category[1] %} 
    <li><a href="{{ post.url }}">{{ post.title }}</a></li> 
  {% endfor %}
</ul>
<p><a href="#{{ category[0] }}-ref">&#8617;</a></p>
{% endfor %}