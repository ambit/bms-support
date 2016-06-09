---
title: Release
permalink: "/news/release/"
position: 3
layout: news
author: all
---

{% for post in site.categories.release %}
  {% include news_item.html %}
{% endfor %}
