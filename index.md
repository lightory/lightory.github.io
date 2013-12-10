---
layout: page
title: Home
---
{% include JB/setup %}

你好，我的名字是刘白光。

这里的表达，是我思考的一个子集。希望这些文字能够跨越时间，且存有价值。

[关于我](/about.html), [全部文章](/archives.html)

### LATEST

<ul class="posts">
  {% for post in site.posts limit:10 %}
  <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>