---
layout: page
show_meta: false
title: "Daftar tutorial dasar clash"
subheadline: "Sitemap Clash"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/basic/"
---
<ul>
    {% for post in site.categories.basic %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>