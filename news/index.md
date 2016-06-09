---
title: News
permalink: "/news/"
position: 27
layout: news
author: all
---

{% for post in site.posts %}
  {% include news_item.html %}
{% endfor %}
