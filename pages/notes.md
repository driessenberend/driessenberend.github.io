---
title: "Notes"
layout: page
permalink: /notes/
---

<ul>
{% for item in site.notes %}
  <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>
