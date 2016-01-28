---
feature:
  name: "Bulleted List"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/19"

layout: default
---

{% capture description %}

The **Bulleted List** feature allows user to create unordered enumeration.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as switch button with "<i class="fa fa-list-ul" aria-label="Bulleted List" title="Bulleted List"></i>" icon
 * Title: "Unordered List" or "Bulleted List"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `ul` element MUST be used to represent the container for **Bulleted List** feature as it's intended to create unorderded lists<sup>[[1](#ref1)]</sup>.

The `li` element MUST be used to represent individual elements inside feature's container as it's intended to mark up all lists' items<sup>[[2](#ref2)]</sup>.

Example:

```
I must buy:
<ul>
	<li>Eggs</li>
	<li>Milk</li>
	<li>Chocolate</li>
</ul>
```

{% endcapture %}

{% capture notes %}

Although this feature should be called "Unordered List", for historical reasons users are used to the "Bulleted List" name. Therefore, for the benefit of learnability, this feature SHOULD be generally referenced as **Bulleted List**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`ul` element definition in HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-ul-element)
2. <a id="ref2"></a>[`li` element definition in HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-li-element)

{% endcapture %}

{% include feature.html %}
