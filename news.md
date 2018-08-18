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
{% include btn.html label="아카이브로 이동" url="{{ "/archive/" | prepend: site.baseurl }}"}