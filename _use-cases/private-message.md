---
case:
  title: "Private Message"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/11"

layout: default
---

{% capture description %}
This use case includes instant messages, e-mails and posts on online forums addressed to one or more recipients. Such messages usually follow the common letter writing conventions [[1](#ref1)]- they start with opening salutations (<i>Dear John</i>, <i>Hello</i>, etc.) and finish with complimentary closing (<i>Best regards</i>, <i>Best wishes</i>, etc.) and the signature of the author.


{% endcapture %}


{% capture features %}

* [Link]({{ site.baseurl }}/features/link.html)
* [Bold]({{ site.baseurl }}/features/bold.html)
* [Italic]({{ site.baseurl }}/features/italic.html)
* [Strikethrough]({{ site.baseurl }}/features/strikethrough.html)
* [Image]({{ site.baseurl }}/features/image.html)
* Quote
* List


{% endcapture %}

{% capture usability %}

* [Emoticons/emojis]({{ site.baseurl }}/usability/enter.html#auto-paragraphing)

{% endcapture %}

{% capture notes %}

* Some private messages might require a subject line, however that is environment specific. However it’s good to note that the subject line should be summarising the content of the message accurately.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[<i>Purdue Online Writing Lab - Personal Letters.</i>](https://owl.english.purdue.edu/owl/resource/992/01/)

{% endcapture %}

{% include use-case.html %}
