---
layout: homepage
---
{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) <small>{{ post.date | date: "%B %d, %Y" }}</small>
{% endfor %}
