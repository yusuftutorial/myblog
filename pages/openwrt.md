---
layout: page
show_meta: false
title: "Daftar tutorial openwrt"
subheadline: "Sitemap Openwrt"
header:
   image_fullwidth: "openwrt.png"
permalink: "/openwrt/"
---
<ul>
    {% for post in site.categories.openwrt %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>