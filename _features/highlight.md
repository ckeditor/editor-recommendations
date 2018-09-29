---
feature:
  name: "Highlight"
  status: "Recommendation"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/63"

description: Recommendation for Highlight feature in WYSIWYG.
layout: default
---

{% capture description %}

The **Highlight** feature marks a part of the text that is relevant in another context.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<span class="fa fa-pencil" title="Highlight" aria-hidden="true"></span><span class="sr-only">Highlight</span>" icon
 * Title: "Highlight"
 * Keystroke: —

{% endcapture %}

{% capture markup %}

The `<mark>` element MUST be used to represent the **Highglight** feature as it is intended to mark parts of content that are relevant in another contexts<sup>[[1](#ref1)]</sup>.

Example:

```html
<p>Find results:</p>
<p>Your <mark>code</mark> is beautiful.</p>
```

{% endcapture %}

{% capture notes %}

**Highlight** feature MAY be used as a mechanism to mark content in the editor found by "Find" or similar feature.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<mark>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/textlevel-semantics.html#the-mark-element).

{% endcapture %}

{% include feature.html %}
