---
layout: page
title: "Blog"
description: ""
---
{% include JB/setup %}

<a href="archive.html">All Posts</a>
<p>
Find by <a href="tags.html"> Tags</a>, <a href="categories.html">Categories</a>
</p>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>