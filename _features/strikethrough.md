---
feature:
  name: "Strikethrough"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/3"

layout: default
---

{% capture description %}

The **Strikethrough** feature marks part of the text that is no longer relevant.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as switch button with "<s>S</s>" icon
 * Title: "Strikethrough"
 * Keystroke: —

{% endcapture %}

{% capture markup %}

The `s` element MUST be used to represent the **Strikethrough** feature as it's intended to mark parts of content that are no longer relevant<sup>[[1](#ref1)]</sup>.

Example:

```
HTML 4 <s>is</s> was the best HTML ever.
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`s` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-s-element)

{% endcapture %}

{% include feature.html %}
