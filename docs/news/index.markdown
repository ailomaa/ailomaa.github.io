---
layout: default
title: News
---

<h3>News</h3>
<ul>
{% for news in site.news %}
  <li><a href="{{ news.url }}">{{ news.title }}</a></li>
{% endfor %}
</ul>
