---
layout: page
title: news
permalink: /news/
nav: true
nav_order: 2
description: News, announcements, conference sessions, and professional activities by Byeonghwa Jeong.
---

{% assign news_items = site.news | sort: "date" | reverse %}

<div class="news">
{% for item in news_items %}
  <div style="margin-bottom: 2rem;">
    <h3>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
    </h3>
    <p class="post-meta">{{ item.date | date: "%B %-d, %Y" }}</p>
  </div>
{% endfor %}
</div>
