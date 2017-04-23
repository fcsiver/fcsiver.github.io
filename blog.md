---
layout: page
title: Research and Nutrition Discussion Board
permalink: /blog/
---

From time to time, I will be updating this page with articles and advice pertaining to nutrition, longevity, and more.
<br><br>
As posts are made, they will be ordered from most recent to least recent.

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
