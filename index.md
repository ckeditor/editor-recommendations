---
title: Home
layout: default
---

{% include home-jumbotron.html %}

{% capture usecases %}

## Use Cases

{% for page in site["use-cases"] %}
### [{{ page.case.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture usability %}

## Usability

{% for page in site.usability %}
### [{{ page.usability.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture features %}

## Editing Features

{% for page in site.features %}
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
