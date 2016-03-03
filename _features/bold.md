---
feature:
  name: "Bold"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/1"

layout: default
---

{% capture description %}

The **Bold** feature marks a part of the text with strong importance.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "**B**" icon
 * Title: "Important" or "Strong Importance"
 * Keystroke: <kbd>Ctrl+B</kbd>

{% endcapture %}

{% capture markup %}

The `<strong>` element MUST be used to represent the **Bold** feature as it is intended to mark parts of content with extra importance<sup>[[1](#ref1)]</sup>.

Example:

```html
This page is about the <strong>Bold</strong> feature.
```

{% endcapture %}

{% capture implementation %}

* The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of the editor users, e.g. change the keystroke to <kbd>Ctrl+Shift+F</kbd> for the German version of UI<sup>[[2](#ref2), [3](#ref3)]</sup>.

{% endcapture %}

{% capture notes %}

Although this feature should be called "Important" or "Strong Importance", for historical reasons users are used to the
"Bold" name. Therefore, for consistency and due to better recognition, this feature SHOULD generally be referred to as **Bold**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<strong>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-strong-element).
2. <a id="ref2"></a>[A discussion about keystrokes in the German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089).
3. <a id="ref3"></a>[An issue about incorrect keystrokes for German and French versions of an editor](https://jira.atlassian.com/browse/CONF-13567).

{% endcapture %}

{% include feature.html %}
