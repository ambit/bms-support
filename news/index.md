---
title: News
permalink: "/news/"
layout: news
author: all
---

{% for post in site.posts %}
  {% include news_item.html %}
{% endfor %}
