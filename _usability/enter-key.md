---
usability:
  title: "Enter Key"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/36"

layout: default
---

{% capture description %}

## Description

<kbd>Enter</kbd> key is used to insert a line break into the editable area. This default behavior could be altered by the context of current selection, type of the content or a modifier key pressed along the <kbd>Enter</kbd> key.

## User Expectations and Popular Behavior

User expects that:

* Pressing the <kbd>Enter</kbd> key would create a new block of text.
* Pressing the <kbd>Shift+Enter</kbd> combination would break a line of text without creating a new block of text.
* The default behavior, defined above, differs when the current selection is in non-paragraph context (e.g. inside heading or list).

## Block context

<a id="autoparagraphing"></a>When the <kbd>Enter</kbd> key is pressed inside a block context, it MUST produce the new block context. If the type of the new block context is not specified by a certain feature, the new block context MUST be a paragraph context and MUST be created by inserting the new `p` element<sup>[[1](#ref1)]</sup> into the current selection position.

When the <kbd>Shift+Enter</kbd> combination is pressed inside a block context, it MUST produce the new line break, by inserting the new `br` element<sup>[[2](#ref2)]</sup> into the current selection position.

## Non-block contexts

If the current selection position does not allow block context, pressing the <kbd>Enter</kbd> key or pressing the <kbd>Shift+Enter</kbd> combination MUST produce the new line break, by inserting the new `br` element<sup>[[2](#ref2)]</sup>.

If the current selection position does not allow block context and does not allow the `br` element, pressing the <kbd>Enter</kbd> key or pressing the <kbd>Shift+Enter</kbd> combination MUST be disabled.

{% endcapture %}

{% capture notes %}

* The behavior of the <kbd>Enter</kbd> key and the <kbd>Shift+Enter</kbd> combination, defined above, SHOULD NOT be altered.

{% endcapture %}

{% capture references %}

1. 	<a id="ref1"></a>[The `p` element definition in the HTML 5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-p-element).
2. <a id="ref2"></a>[The `br` element definition in the HTML 5 standard](https://www.w3.org/TR/html5/text-level-semantics.html#the-br-element).

{% endcapture %}

{% include usability.html %}
