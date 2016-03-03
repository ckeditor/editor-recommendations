---
feature:
  name: "Numbered List"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/19"

layout: default
---

{% capture description %}

The **Numbered List** feature allows the user to create ordered enumeration.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<i class="fa fa-list-ol" aria-label="Numbered List" title="Numbered List"></i>" icon
 * Title: "Ordered List" or "Numbered List"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<ol>` element MUST be used to represent the container for the **Numbered List** feature as it is intended to create ordered lists<sup>[[1](#ref1)]</sup>.

The `<li>` element MUST be used to represent individual elements inside the feature's container as it is intended to mark up all list items<sup>[[2](#ref2)]</sup>.

Example:

```html
In case of emergency:
<ol>
	<li>Commit all your changes to Git.</li>
	<li>Jump out of the window.</li>
</ol>
```

{% endcapture %}

{% capture notes %}

Although this feature should be called "Ordered List", for historical reasons users are used to the "Numbered List" name. Therefore, for consistency and due to better recognition, this feature SHOULD generally be referred to as **Numbered List**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<ol>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-ol-element).
2. <a id="ref2"></a>[The `<li>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-li-element).

{% endcapture %}

{% include feature.html %}
