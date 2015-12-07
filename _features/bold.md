---
feature:
  name: "Bold"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/1"

layout: default
---

{% capture description %}

The **Bold** feature marks part of the text with strong importance.

{% endcapture %}

{% capture ui %}

 * UI: ON/OFF feature, usually represented as switch button with "**B**" icon
 * Title: "Important" or Strong Importance"
 * Keystroke: <kbd>CTRL+B</kbd>

{% endcapture %}

{% capture markup %}

The `strong` element MUST be used to represent the **Bold** feature as it's intended to mark parts of content with extra importance<sup>[[1](#ref1)]</sup>.

Example:

```
This page is about the <strong>Bold</strong> feature.
```

{% endcapture %}

{% capture implementation %}

* The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of users of the editor, eg. change keystroke to <kbd>CTRL+SHIFT+F</kbd> for German version of UI<sup>[[2](#ref2), [3](#ref3)]</sup>.

{% endcapture %}

{% capture notes %}

Although this feature SHOULD be called "Important" or "Strong Importance", for historical reasons users are used to the
"Bold" name. Therefore, for the benefit of learnability, this feature SHOULD be generally referenced as **Bold**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`strong` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-strong-element)
2. <a id="ref2"></a>[Discussion about keystrokes in German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089)
3. <a id="ref3"></a>[Issue about incorrect keystrokes for German and French versions of editor](https://jira.atlassian.com/browse/CONF-13567)

{% endcapture %}

{% include feature.html %}
