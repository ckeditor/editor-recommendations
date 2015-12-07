---
feature:
  name: "Italic"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/2"

layout: default
---

{% capture description %}

The **Italic** feature marks part of the text with emphatic stress.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as switch button with "*I*" icon
 * Title: "Emphatic Stress"
 * Keystroke: <kbd>CTRL+I</kbd>

{% endcapture %}

{% capture markup %}

The `em` element MUST be used to represent the **Italic** feature, as it's the element dedicated to mark stress emphasis<sup>[[1](#ref1)]</sup>.

Example:

```
The Italic feature is also known as <em>Emphatic Stress</em>.
```

{% endcapture %}

{% capture implementation %}

* The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of users of the editor, eg. change keystroke to <kbd>CTRL+SHIFT+K</kbd> for German version of UI<sup>[[2](#ref2), [3](#ref3)]</sup>.

{% endcapture %}

{% capture notes %}

Although this feature SHOULD be called "Emphatic Stress", for historical reasons users are used to the "Italic" name.
Therefore, for the benefit of learnability, this feature SHOULD be generally referenced as **Italic**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`em` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-em-element)
2. <a id="ref2"></a>[Discussion about keystrokes in German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089)
3. <a id="ref3"></a>[Issue about incorrect keystrokes for German and French versions of editor](https://jira.atlassian.com/browse/CONF-13567)

{% endcapture %}

{% include feature.html %}
