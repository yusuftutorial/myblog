---
layout: page
show_meta: false
title: "Aplikasi"
subheadline: "Sitemap Aplikasi"
header:
   image_fullwidth: "aplikasi.png"
permalink: "/aplikasi/"
---
<ul>
    {% for post in site.categories.aplikasi %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>