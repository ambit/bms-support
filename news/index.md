---
title: News
permalink: "/news/"
position: 23
layout: news
author: all
---

{% for post in site.posts %}
  {% include news_item.html %}
{% endfor %}
