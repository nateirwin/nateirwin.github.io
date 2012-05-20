---
layout: main
sitemap:
  priority: 1.0
  changefreq: daily
  lastmod: 2012-05-20T09:45:19-06:00
title: Web mapping, technology, and life
---

{% for post in site.posts limit:3 %}
  <div class="span12 post">
    <h1>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
    <span class="meta">
      Posted on {{ post.date | date_to_string }}
    </span>
    <div class="tw_button">
      <a href="https://twitter.com/share" class="twitter-share-button" data-url="http://nateirwin.net{{ post.url }}" data-via="nateirwin">Tweet</a>
    </div>
    {{ post.content }}
    <hr>
  </div>
{% endfor %}
{% for post in site.posts limit:9 offset:3 %}
  <div class="span4">
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <span class="meta">
      {{ post.date | date_to_string }}
    </span>
  </div>
{% endfor %}