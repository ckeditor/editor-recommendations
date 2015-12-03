---
feature:
  name: "Bold"
  status: "Draft"

layout: default
---

{% capture description %}

The **Bold** feature marks part of the text with strong importance.

{% endcapture %}

{% capture ui %}

 * UI: switch button with "**B**" icon
 * Title: "Strong Importance"
 * Keystroke: <kbd>CTRL+B</kbd>

{% endcapture %}

{% capture markup %}

The `strong` element MUST be used to represent the **Bold** feature as it's intended to mark parts of content with extra importance<sup>[[1](#ref1)]</sup>.

Example:

```
This page is about the <strong>Bold</strong> feature.
```

{% endcapture %}

{% capture misconceptions %}

* The purpose of **Bold** feature is to mark some part of text as consisting semantically important content. Therefore `b` element MUST NOT be used to represent that feature as it's intended to visually distinguish some parts of content without conveying any extra importance<sup>[[2](#ref2)]</sup>.

{% endcapture %}

{% capture implementation %}

### Internationalization

The UI and keystroke are optimized for English language, therefore it MAY be considered to adjust them to the native language of users of the editor, eg. change keystroke to <kbd>CTRL+SHIFT+F</kbd> for German version of UI<sup>[[3](#ref3), [4](#ref4)]</sup>.

{% endcapture %}

{% capture notes %}

Although this feature SHOULD be called "Important" or "Strong Importance", for historical reasons users are used to the
"Bold" name. Therefore, for the benefit of learnability, this feature SHOULD be generally referenced as **Bold**.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`strong` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-strong-element)
2. <a id="ref2"></a>[`b` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-b-element)
3. <a id="ref3"></a>[Discussion about keystrokes in German version of Word](http://dict.leo.org/forum/viewGeneraldiscussion.php?idThread=846089)
4. <a id="ref4"></a>[Issue about incorrect keystrokes for German and French versions of editor](https://jira.atlassian.com/browse/CONF-13567)

{% endcapture %}

{% include feature.html %}
