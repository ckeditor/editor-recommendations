---
title: Home
layout: default
jumbotron: true
---

{% capture usecases %}

{% for page in site["use-cases"] %}
### [{{ page.case.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture usability %}

{% for page in site.usability %}
### [{{ page.usability.title }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}

{% capture features %}

{% for page in site.features %}
### [{{ page.feature.name }}]({{ site.baseurl }}{{ page.url }})
{% endfor %}

{% endcapture %}


<div class="row">
  <div class="col-md-6">
    <h2 class="page-header">Editing Features</h2>
    {{ features | markdownify }}
  </div>
  <div class="col-md-6">
    <h2 class="page-header">Use Cases</h2>
    {{ usecases | markdownify }}
    <h2 class="page-header">Usability</h2>
    {{ usability | markdownify }}
  </div>
</div>
