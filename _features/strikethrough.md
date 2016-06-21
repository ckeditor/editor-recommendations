---
feature:
  name: "Strikethrough"
  description: Draft for Strikethrough feature in WYSIWYG.
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/3"

layout: default
---

{% capture description %}

The **Strikethrough** feature marks a part of the text that is no longer relevant.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<i class="fa fa-strikethrough" title="Strikethrough" aria-hidden="true"></i><span class="sr-only">Strikethrough</span>" icon
 * Title: "Strikethrough"
 * Keystroke: —

{% endcapture %}

{% capture markup %}

The `<s>` element MUST be used to represent the **Strikethrough** feature as it is intended to mark parts of content that are no longer relevant<sup>[[1](#ref1)]</sup>.

Example:

```html
HTML 4 <s>is</s> was the best HTML ever.
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<s>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-s-element).

{% endcapture %}

{% include feature.html %}
