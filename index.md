---
title: Home
layout: default
---

{% include home-jumbotron.html %}

{% capture usecases %}

## Use Cases

### [Blog / Article]()

### [Article Comments]()

### [Rich-Text Fields]()

{% endcapture %}

{% capture usability %}

## Usability

### [Enter Key]()

### [Smart Typing]()

{% endcapture %}

{% capture features %}

## Editing Features

{% for page in site.collections.features.docs %}
### [{{ page.feature.name }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}


<div class="row">
  <div class="col-md-6">
    {{ usecases | markdownify }}
    {{ usability | markdownify }}
  </div>
  <div class="col-md-6">
    {{ features | markdownify }}
  </div>
</div>
