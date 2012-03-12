---
layout: page
title: Lonely Planet
---
{% include JB/setup %}

> 我们全都需要有人注视我们。根据我们生活所追求的不同的目光类型，可以将我们分成四类。第一类人追求那种被无数不知名的人注视的眼光，换句话说，就是公众的目光。第二类是那种离开了众多双熟悉的眼睛注视的目光就活不下去的人。他们是鸡尾酒会与聚餐中永不疲倦的主人。第三类人，他们必须活在所爱之人的目光下。他们和第一类人同样都置身于危险处境，一旦所爱的人闭上双眼，其生命殿堂也将陷入黑暗之中。最后是第四类，这一类人最少。他们是梦想家，生活在想象中某一双远方的眼睛之下。

### 最近发布的文章

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>