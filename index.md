---
title: Home
layout: default
---

# The Editor Recommendation Project

This is a website made with Jekyll.

## Editing Features

{% for page in site.collections.features.docs %}
  <h3><a href="{{ page.url }}">{{ page.feature.name }}</a></h3>
{% endfor %}


