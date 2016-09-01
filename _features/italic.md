---
feature:
  name: "Italic"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/2"

description: Draft for Italic feature in WYSIWYG.
layout: default
---

{% capture description %}

The **Italic** feature marks a part of the text offset from the normal prose in a manner indicating a different quality of text.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "<i class="fa fa-italic" title="Italic" aria-hidden="true"></i><span class="sr-only">Italic</span>" icon
 * Title: "Italic"
 * Keystroke: <kbd>Ctrl+I</kbd>

{% endcapture %}

{% capture markup %}

The `i` element MUST be used to represent the **Italic** feature, as it's the element dedicated to mark a a different quality of text, such as taxonomic designation, a technical term or an idiomatic phrase<sup>[[1](#ref1)]</sup>.

Example:

```html
The Italic feature is a <i>de facto</i> standard in Rich Text Editors.
```

{% endcapture %}

{% capture implementation %}

* The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of the editor users, e.g. change the keystroke to <kbd>Ctrl+Shift+K</kbd> for the German version of UI<sup>[[2](#ref2), [3](#ref3)]</sup>.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<i>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/text-level-semantics.html#the-i-element).
2. <a id="ref2"></a>[A discussion about keystrokes in the German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089).
3. <a id="ref3"></a>[An issue about incorrect keystrokes for German and French versions of an editor](https://jira.atlassian.com/browse/CONF-13567).

{% endcapture %}

{% include feature.html %}
