---
layout: page
title: News
description: >-
  Short research, publication, and professional updates from Aaron P. Ledray.
permalink: /news/
---

# News

{% assign news_items = site.data.news | sort: 'date' | reverse %}
{% if news_items.size > 0 %}
<ul class="news-list">
  {% for item in news_items %}
    <li class="news-item">
      <time datetime="{{ item.date | date: '%Y-%m-%d' }}">{{ item.date | date: "%B %-d, %Y" }}</time>
      <p><strong>{{ item.title | escape }}</strong>{% if item.text %}: {{ item.text | escape }}{% endif %}</p>
      {% if item.link %}<p><a href="{{ item.link | escape }}">{{ item.link_label | default: "Read more" | escape }}</a></p>{% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>Nothing new to share just yet. Check back soon.</p>
{% endif %}
