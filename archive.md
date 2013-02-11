---
layout: page
title: Archive
---

# Archive

{% for post in site.posts %}
  {% unless post.next %}
<h2>{{ post.date | date: '%Y' }}</h2><ul><li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% else %}
    {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
    {% if year != nyear %}
</ul><h2>{{ post.date | date: '%Y' }}</h2><ul><li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% else %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endunless %}
{% endfor %}