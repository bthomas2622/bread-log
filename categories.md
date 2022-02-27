---
layout: page
title: Index
permalink: /categories-list/
---

<ul>
{% for category in site.categories %}
  <li><b><a name="{{ category | first }}">{{ category | first }}</a></b>
    <ul>
    {% for post in category.last %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>