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

 * UI: The **Bold** feature is usually represented in the toolbar as an ON/OFF feature.
 * Title: "Strong Importance"
 * Keystroke: <kbd>CTRL+B</kbd>

{% endcapture %}

{% capture markup %}

The `strong` element must be used to represent the **Bold** feature.

Example:

```
This page is about the <strong>Bold</strong> feature.
```

{% endcapture %}

{% capture notes %}

Although this feature should be called "Important" or "Strong Importance", for historical reasons users are used to the
"Bold" name. Therefore, for the benefit of learnability, this feature should be generally referenced as **Bold**.

{% endcapture %}

{% include feature.html %}