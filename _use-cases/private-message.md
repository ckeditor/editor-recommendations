---
case:
  title: "Private Message"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/11"

layout: default
---

{% capture description %}

This use case includes instant messages, e-mails and posts on online forums addressed to one or more recipients. Such messages usually follow the common letter writing conventions<sup>[[1](#ref1)]</sup> &mdash; they start with an opening salutation (<i>Dear John</i>, <i>Hello</i>, etc.) and finish with a complimentary closing (<i>Best regards</i>, <i>Best wishes</i>, etc.) and the signature of the author.

{% endcapture %}

{% capture features %}

* [Link]({{ site.baseurl }}/features/link.html)
* [Bold]({{ site.baseurl }}/features/bold.html)
* [Italic]({{ site.baseurl }}/features/italic.html)
* [Strikethrough]({{ site.baseurl }}/features/strikethrough.html)
* [Image]({{ site.baseurl }}/features/image.html)
* [Quote]({{ site.baseurl}}/features/quote.html)
* [Bulleted List]({{ site.baseurl }}/features/bulleted-list.html)
* [Numbered List]({{ site.baseurl }}/features/numbered-list.html)
* Emoticons/Emojis

{% endcapture %}

{% capture usability %}

{% endcapture %}

{% capture notes %}

* Some private messages might require a subject line; this is, however, environment-specific. The subject line is intended to accurately summarise the content of the message.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[<i>Purdue Online Writing Lab - Personal Letters.</i>](https://owl.english.purdue.edu/owl/resource/992/01/)

{% endcapture %}

{% include use-case.html %}
