---
layout: main
---

{% for post in site.posts limit:3 %}
<div class="row-fluid">
  <div class="span12 post">
    <h1>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
    <span class="meta">
      Posted on {{ post.date | date_to_string }}
    </span>
    {{ post.content }}
    {% if post.via and post.viaurl %}
      <p>
        (Via <a href="{{post.viaurl}}">{{post.via}}</a>)
      </p>
    {% endif %}
    <hr>
  </div>
</div>
{% endfor %}
<div class="row-fluid">
{% for post in site.posts limit:3 offset:3 %}
  <div class="span4">
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <span class="meta">
      {{ post.date | date_to_string }}
    </span>
    {{ post.content | truncatewords: 30 | strip_html }}
  </div>
{% endfor %}
</div>
<div class="row-fluid">
{% for post in site.posts limit:3 offset:6 %}
  <div class="span4">
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <span class="meta">
      {{ post.date | date_to_string }}
    </span>
    {{ post.content | truncatewords: 30 | strip_html }}
  </div>
{% endfor %}
</div>
<div class="row-fluid">
{% for post in site.posts limit:3 offset:9 %}
  <div class="span4">
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <span class="meta">
      {{ post.date | date_to_string }}
    </span>
    {{ post.content | truncatewords: 30 | strip_html }}
  </div>
{% endfor %}
</div>