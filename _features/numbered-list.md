---
feature:
  name: "Numbered List"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/19"

description: Draft for Numbered List feature in WYSIWYG.
layout: default
---

{% capture description %}

The **Numbered List** feature allows the user to create ordered enumeration.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<i class="fa fa-list-ol" title="Numbered List" aria-hidden="true"></i><span class="sr-only">Numbered List</span>" icon
 * Title: "Ordered List" or "Numbered List"
 * Keystroke: –
 * Additional keyboard behavior:
   * <kbd>Backspace</kbd> inside an empty list item or at the beginning of a non-empty list item SHOULD join the current list item with the previous list item, if that item exists, otherwise transform current list item into the default block context.
   * <kbd>Delete</kbd> inside an empty list item or at the end of a non-empty list item SHOULD join the next block context of any type with the current list item.
   * <kbd>Backspace</kbd> or <kbd>Delete</kbd> inside an empty list item, that is the only list item in the list, SHOULD replace the whole list with the default block context.
   * <kbd>Tab</kbd> at the beginning of a non-empty list item or inside an empty list item SHOULD indent the current list item, if the list item is allowed to be indented.
   * <kbd>Shift+Tab</kbd> inside an indented list item SHOULD outdent the current list item.
   * <kbd>Enter</kbd> inside a non-empty list item SHOULD insert a new list item before the current list item.
   * <kbd>Enter</kbd> inside an empty, indented list item SHOULD outdent the current list item.
   * <kbd>Enter</kbd> inside an empty, non-indented list item SHOULD create a new default block context, following the list. If there are list items following the current list item, the list SHOULD be split into two lists, separated by the newly created default block context.

{% endcapture %}

{% capture markup %}

The `<ol>` element MUST be used to represent the container for the **Numbered List** feature as it is intended to create ordered lists<sup>[[1](#ref1)]</sup>.

The `<li>` element MUST be used to represent individual elements inside the feature's container as it is intended to mark up all list items<sup>[[2](#ref2)]</sup>.

Example:

```html
<p>In case of emergency:</p>
<ol>
	<li>Commit all your changes to Git.</li>
	<li>Jump out of the window.</li>
</ol>
```

{% endcapture %}

{% capture implementation %}

  * <kbd>Tab</kbd> key is generally used to steer focus from and into the editor and overwriting its behavior could be misleading. Therefore the following key bindings MAY be used instead of the <kbd>Tab</kbd> key<sup>[[3](#ref3)]</sup>:
    * <kbd>Ctrl+M</kbd> for indenting,
    * <kbd>Ctrl+Shift+M</kbd> for outdenting.

{% endcapture %}

{% capture notes %}

Although this feature should be called "Ordered List", for historical reasons users are used to the "Numbered List" name. Therefore, for consistency and due to better recognition, this feature SHOULD generally be referred to as **Numbered List**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<ol>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-ol-element).
2. <a id="ref2"></a>[The `<li>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-li-element).
3. <a id="ref3"></a>[The description of Rich Text Editor use case in <i>WAI-ARIA 1.0 Authoring Practices</i>](https://www.w3.org/TR/wai-aria-practices/#richtext).

{% endcapture %}

{% include feature.html %}
