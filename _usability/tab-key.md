---
usability:
  title: "Tab Key"
  status: "Recommendation"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/41"

description: Recommendation for Tab key behavior in WYSIWYG.
layout: default
---

{% capture description %}

<kbd>Tab</kbd> key is used to steer the focus into and from the editor.

{% endcapture %}

{% capture expectations %}

User expects that:

* when the element preceding the editor is focused, pressing <kbd>Tab</kbd> key would focus the editor;
* when the editor is focused, pressing <kbd>Tab</kbd> key would move focus outside the editor.

{% endcapture %}

{% capture recommendations %}

### Steering focus into the editor<sup>[[1](#ref1)]</sup>

If the focusable element directly preceding the editor in the page's focus order is focused, pressing <kbd>Tab</kbd> key MUST move the focus inside the editable area.

If the element directly succeeding the editor in the page's focus order is focused, pressing <kbd>Shift+Tab</kbd> key combination MUST move the focus inside the editable area.

If the editor is outside the current visible area of the page, the editor MUST be scrolled inside the current visible area of the page.

When the focus is moved inside the editable area, the previous selection state, if it exists, MUST be restored.

### Steering focus away from the editor<sup>[[1](#ref1)]</sup>

If the editable area is focused, pressing <kbd>Tab</kbd> key MUST move the focus to the focusable element directly succeeding the editor in the page's focus order.

If the editable area is focused, pressing <kbd>Shift+Tab</kbd> key combination MUST move the focus to the focusable element directly preceding the editor in the page's focus order.

When the focus is about to be moved away from the editable area, the current selection state MUST be saved to be restored when the editable area regains focus.

{% endcapture %}

{% capture notes %}

* The overwriting of the default behavior of the <kbd>Tab</kbd> key and the <kbd>Shift+Tab</kbd> key combination, defined above, in certain features is possible, however accessibility issues SHOULD be taken into consideration.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The description of Rich Text Editor use case in <i>WAI-ARIA 1.0 Authoring Practices</i>](https://rawgit.com/w3c/aria-practices/master/aria-practices-DeletedSectionsArchive.html#richtext).

{% endcapture %}

{% include usability.html %}
