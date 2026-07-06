---
layout: page
title: Music
---

This is where I showcase all things musically related.
In the past, I have featured my compositions, recordings, and musical recommendations here.
See below for a list of blog posts related to music.

{% for tag in site.tags %}
{% if tag[0] == "music" %}
{% for post in tag[1] %}

## [{{ post.title }}]({{ post.url }})
<span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
{{ post.excerpt }}
[*see more...*]({{ post.url }})

{% endfor %}
{% endif %}
{% endfor %}
