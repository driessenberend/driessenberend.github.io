---
title: "Blog"
layout: page
permalink: /blog/
---

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

<ul>
{% for post in posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <small>— {{ post.date | date: "%-d %b %Y" }}</small>
  </li>
{% endfor %}
</ul>

{% if paginator %}
<nav class="pager">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">← Vorige</a>
  {% endif %}
  <span>Pagina {{ paginator.page }} van {{ paginator.total_pages }}</span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Volgende →</a>
  {% endif %}
</nav>
{% endif %}

