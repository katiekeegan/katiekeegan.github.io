---
layout: homepage
permalink: /blog.html
---
{% for post in site.posts %}
<article class="post-preview">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p class="post-date"><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
  <div class="post-excerpt">
    {% if post.excerpt %}
      {{ post.excerpt | strip_html | truncatewords: 50 }}
    {% else %}
      {{ post.content | strip_html | truncatewords: 50 }}
    {% endif %}
    <a href="{{ post.url }}">Read more</a>
  </div>
</article>
<hr>
{% endfor %}
