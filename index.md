---
layout: index
title: John Doe
tagline: aka nickname
---
{% include JB/setup %}


<!-- Change the "about information" contained in /_includes/themes/bootstrap/index.html  -->

<h3>Sample "posts list"</h3>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
