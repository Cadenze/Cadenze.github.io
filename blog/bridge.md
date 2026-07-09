---
layout: page
title: Bridge
---

Bridge is a trick-taking card game for 4 people,
played as two pairs of teammates.
With 13 total available tricks,
the goal of the game is to take, along with your partner,
as many tricks as possible,
and somehow predetermine, before playing a single card,
approximately how many tricks you are going to make.

If you are interested,
I have written a [guide](/2026/07/08/how-to-play-bridge)
to teach the game from first principles;
or if you are an advanced player,
see below for my thoughts on bidding and play.

{% for tag in site.tags %}
{% if tag[0] == "bridge" %}
{% for post in tag[1] %}

## [{{ post.title }}]({{ post.url }})
<span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
{{ post.excerpt }}
[*see more...*]({{ post.url }})

{% endfor %}
{% endif %}
{% endfor %}
