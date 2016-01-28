---
feature:
  name: "Numbered List"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/19"

layout: default
---

{% capture description %}

The **Numbered List** feature allows user to create ordered enumeration.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as switch button with "<i class="fa fa-list-ol" aria-label="Numbered List" title="Numbered List"></i>" icon
 * Title: "Ordered List" or "Numbered List"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `ol` element MUST be used to represent the container for **Numbered List** feature as it's intended to create orderded lists<sup>[[1](#ref1)]</sup>.

The `li` element MUST be used to represent individual elements inside feature's container as it's intended to mark up all lists' items<sup>[[2](#ref2)]</sup>.

Example:

```
In case of emergency:
<ol>
	<li>Commit all your changes to Git;</li>
	<li>Jump out of window.</li>
</ol>
```

{% endcapture %}

{% capture notes %}

Although this feature should be called "Ordered List", for historical reasons users are used to the "Numbered List" name. Therefore, for the benefit of learnability, this feature SHOULD be generally referenced as **Numbered List**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`ol` element definition in HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-ol-element)
2. <a id="ref2"></a>[`li` element definition in HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-li-element)

{% endcapture %}

{% include feature.html %}
