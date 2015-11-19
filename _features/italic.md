---
feature:
  name: "Italic"
  status: "Draft"

layout: default
---

{% capture description %}

The **Italic** feature marks part of the text with emphatic stress.

{% endcapture %}

{% capture ui %}

 * UI: The **Italic** feature is usually represented in the toolbar as an ON/OFF feature.
 * Title: "Emphatic Stress"
 * Keystroke: <kbd>CTRL+I</kbd>

{% endcapture %}

{% capture markup %}

The `em` element must be used to represent the **Italic** feature.

Example:

```
The Italic feature is also known as <em>Emphatic Stress</em>.
```

{% endcapture %}

{% capture notes %}

Although this feature should be called "Emphatic Stress", for historical reasons users are used to the "Italic" name.
Therefore, for the benefit of learnability, this feature should be generally referenced as **Italic**.

{% endcapture %}

{% include feature.html %}
