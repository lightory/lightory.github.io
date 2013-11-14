---
layout: page
title: Lonely Planet
---
{% include JB/setup %}

### LATEST

<ul class="posts">
  {% for post in site.posts limit:6 %}
  <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

### ABOUT ME

你好，我的名字是刘白光。

你也可以称呼我为 Light 或 Lightory，这是我在网上所惯用的 ID。你能够在 [Twitter](http://twitter.com/lightory/), [Weibo](http://weibo.com/lightory/), [Douban](http://douban.com/people/lightory/) 找到我。

我出生于 1990，在世间已经二十余年，却依旧一事无成。

我目前居住在上海，从事互联网行业，具体而言，在一家 Startup。然而，我并不能够确定，在你读到这些文字的时间点，我身在何处，又在做一些什么。未来总是充满了不确定性，这正是世界的迷人之处。

既然你在阅读这些文字，多半是对我产生了一些兴趣，不妨给我写一封邮件，我的邮箱是 <lightory@gmail.com>。

### BRIEF

- 1990 年出生于江西萍乡。
- 2007 年 7 月至 2011 年 6 月就读于南京大学地球科学与工程学院。有《[我在南大的四年](http://lightory.github.io/2011/06/11/four-years-in-nju)》一文。
- 2010 年 7 月至 9 月在腾讯公司实习，从事手机产品设计。
- 2011 年下半年，在[百姓网](http://baixing.com)任产品管理工程师。
- 2012 年初至今，参与创办[火花](http://huohua.in)。