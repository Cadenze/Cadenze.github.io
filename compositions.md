---
layout: default
title: Compositions
---

Not much is going on here as of now, but congratulations for finding this page.

{% for composition in site.compositions %}
  * {{ composition.date | date_to_string }} &mdash; [ {{ composition.title }} ]({{ composition.url }})
{% endfor %}