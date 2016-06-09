---
title: News
permalink: "/news/"
position: 22
layout: news
author: all
---

{% for post in site.posts %}
  {% include news_item.html %}
{% endfor %}
