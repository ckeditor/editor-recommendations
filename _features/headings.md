---
feature:
  name: "Headings"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/43"

description: Draft for Headings feature in WYSIWYG.
layout: default
---

{% capture description %}

The **Headings** feature allows user to divide the content via inserting headers into it.

{% endcapture %}

{% capture ui %}

 * UI: usually represented as a part of "Styles" dropdown or "Styles" menu on a ribbon
 * Title: "Heading &lt;x&gt;", where "&lt;x&gt;" is a natural number indicating the heading's level
 * Keystroke: <kbd>Ctrl+Shift+&lt;x&gt;</kbd>, where "&lt;x&gt;" is a natural number indicating the heading's level
 * Additional keyboard behavior:
   * <kbd>Enter</kbd> at the end of the heading SHOULD create an empty, default block context directly after the heading and move selection position inside the newly created block context.
   * <kbd>Enter</kbd> at the beginning or inside the heading SHOULD split the heading into two heading block contexts just before the selection position
   * <kbd>Shift+Enter</kbd> at the beginning or inside the heading SHOULD insert a line break just before the selection position

{% endcapture %}

{% capture markup %}

The editor SHOULD allow to insert three levels of headings, that MUST be represented by the following HTML elements<sup>[[1](#ref1)]</sup>:

* **Heading Level 1** – `<h2>` element
* **Heading Level 2** – `<h3>` element
* **Heading Level 3** – `<h4>` element

Example:

```html
<h2>Heading 1</h2>
<p>Some text.</p>
```

{% endcapture %}

{% capture implementation %}

* If there is a need to provide more levels of headings, editor MAY allow to insert deeper levels by utilizing `<h5>` and `<h6>` elements<sup>[[1](#ref1)]</sup> with optional `[aria-level]`<sup>[[2](#ref2)]</sup> attribute.
* In the vast majority of use cases, the content created using the editor would be a part of a page, therefore usage of `<h1>` element is highly unrecommended<sup>[[3](#ref3), [4](#ref4)]</sup>. However if the content of the editor would be presented in an independent form, `<h1>` element MAY be used<sup>[[1](#ref1)]</sup>. Implementer MAY think of naming this level of heading in a more distinguishable way e.g. "Title".

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` elements definition in the HTML5 standard](https://www.w3.org/TR/html5/sections.html#the-h1,-h2,-h3,-h4,-h5,-and-h6-elements).
2. <a id="ref2"></a>[The description of `[aria-level]` attribute in the ARIA 1.0 standard](https://www.w3.org/TR/wai-aria/states_and_properties#aria-level).
3. <a id="ref3"></a>[<i>Creating an outline</i> section in the HTML5 standard](https://www.w3.org/TR/html5/sections.html#outlines).
4. <a id="ref4"></a>[Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).

{% endcapture %}

{% include feature.html %}
