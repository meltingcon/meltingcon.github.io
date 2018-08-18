---
layout: page
title : 새 소식
permalink: /news/
---

{% for post in site.posts limit:20 %}
## [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
- {{ post.date | date: "%Y.%m.%d" }}{% if post.author %} | {{ post.author }}{% endif %}
- {{ post.content | strip_html | truncatewords:50 }}
{% endfor %}

<a class="button is-warning is-inverted is-outlined"
  href="{{ "/archive/" | prepend: site.baseurl }}">아카이브로 이동</a>