---
feature:
  name: "Bulleted List"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/19"

layout: default
---

{% capture description %}

The **Bulleted List** feature allows the user to create unordered enumeration.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<i class="fa fa-list-ul" aria-label="Bulleted List" title="Bulleted List"></i>" icon
 * Title: "Unordered List" or "Bulleted List"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<ul>` element MUST be used to represent the container for the **Bulleted List** feature as it is intended to create unorderded lists<sup>[[1](#ref1)]</sup>.

The `<li>` element MUST be used to represent individual elements inside the feature's container as it is intended to mark up all list items<sup>[[2](#ref2)]</sup>.

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

Although this feature should be called "Unordered List", for historical reasons users are used to the "Bulleted List" name. Therefore, for consistency and due to better recognition, this feature SHOULD generally be referred to as **Bulleted List**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<ul>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-ul-element).
2. <a id="ref2"></a>[The `<li>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-li-element).

{% endcapture %}

{% include feature.html %}
