---
title: Tags | joelchrono12
header: Tags
description: Specific themes I like to talk about
permalink: /tags/
layout: default
---

These are the current available tags, as well as the RSS feed of each of them, in case you want to follow certain topics , I still have to make this look pretty, but it works.

{% for tag in site.tags %}
  <h2>{{ tag[0] }}</h2>
  <a href="/tags/{{ tag[0] }}/" class="button">All posts</a> <a class="button" href="/feeds/{{ tag[0] }}.xml/">RSS</a>
  <ul>
    {% for post in tag[1] limit:2 %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> - 📅 {{post.date | date_to_string}} </li>
    {% endfor %}
  </ul>

{% endfor %}
