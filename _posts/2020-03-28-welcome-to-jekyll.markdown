---
layout: default
title:  "Vse slike"
date:   2020-03-28 21:17:15 +0100
categories: jekyll update
---

<h1>Mape fotografij:</h1>
<ul>
  {% comment %}
    Get all "photo_set" pages and display a list with links to them.
  {% endcomment %}
  {% assign photo_pages = site.pages | where: "layout", "gallery" %}
  {% for photo_page in photo_pages %}
    <li>
      <a href="{{ photo_page.url | prepend: site.baseurl }}">{{ photo_page.title }}</a>
    </li>
  {% endfor %}
</ul>