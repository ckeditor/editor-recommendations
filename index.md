---
title: Home
layout: default
---

{% include home-jumbotron.html %}

## Editing Features

{% for page in site.collections.features.docs %}
  <h3><a href="{{ site.baseurl }}{{ page.url }}">{{ page.feature.name }}</a></h3>
{% endfor %}


