---
feature:
  name: "Italic"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/2"

layout: default
---

{% capture description %}

The **Italic** feature marks a part of the text with emphatic stress.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as a switch button with the "*I*" icon
 * Title: "Emphatic Stress"
 * Keystroke: <kbd>Ctrl+I</kbd>

{% endcapture %}

{% capture markup %}

The `em` element MUST be used to represent the **Italic** feature, as it's the element dedicated to mark stress emphasis<sup>[[1](#ref1)]</sup>.

Example:

```html
The Italic feature is also known as <em>Emphatic Stress</em>.
```

{% endcapture %}

{% capture implementation %}

* The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of the editor users, e.g. change the keystroke to <kbd>Ctrl+Shift+K</kbd> for the German version of UI<sup>[[2](#ref2), [3](#ref3)]</sup>.

{% endcapture %}

{% capture notes %}

Although this feature should be called "Emphatic Stress", for historical reasons users are used to the "Italic" name.
Therefore, for consistency and due to better recognition, this feature SHOULD generally be referred to as **Italic**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<em>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-em-element).
2. <a id="ref2"></a>[A discussion about keystrokes in the German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089).
3. <a id="ref3"></a>[An issue about incorrect keystrokes for German and French versions of an editor](https://jira.atlassian.com/browse/CONF-13567).

{% endcapture %}

{% include feature.html %}
