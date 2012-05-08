---
layout: page
title: 
tagline:
---
{% include JB/setup %}

## Latest Updates
<div style="width: 350px; float:left" >
<br>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
</div>
<div float="right">
	<img src="mhetrick2.jpg" width="570" height="604" align="right" />
</div>
