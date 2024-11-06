---
layout: default
---

<h3>News</h3>
<ul>
{% for post in site.categories["news"] %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
