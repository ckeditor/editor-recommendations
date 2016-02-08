---
title: Home
layout: default
jumbotron: true
---

{% capture usecases %}

## Use Cases

{% for page in site.collections["use-cases"].docs %}
### [{{ page.case.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture usability %}

## Usability

{% for page in site.collections.usability.docs %}
### [{{ page.usability.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture features %}

## Editing Features

{% for page in site.collections.features.docs %}
### [{{ page.feature.name }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}


<div class="row">
  <div class="col-md-6">
    {{ features | markdownify }}
  </div>
  <div class="col-md-6">
    {{ usecases | markdownify }}
    {{ usability | markdownify }}
  </div>
</div>
