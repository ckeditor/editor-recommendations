---
case:
  title: "Article Comments"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/42"

description: Draft for Article Comments WYSIWYG use-case.
layout: default
---

{% capture description %}

It is a common practice that most of the blogs allow their users to comment the published posts. The ability to comment is usually represented by a simple form with a textfield for the comment's content. That textfield allows users to write a comment and add some basic styling to it (e.g. bold, underline) and comment on particular quotes from the text. The ability to include images in the comments is gaining popularity.

{% include figures/thumbnail.html src="use_case/article-comments/fig-1.png" alt="An example of an article comment, showing a few of the most frequently used features: quotes, links and bold" caption="A basic form of an article comment." %}

{% endcapture %}

{% capture features %}

* [Link]({{ site.baseurl }}/features/link.html)
* [Bold]({{ site.baseurl }}/features/bold.html)
* [Italic]({{ site.baseurl }}/features/italic.html)
* [Strikethrough]({{ site.baseurl }}/features/strikethrough.html)
* [Quote]({{ site.baseurl}}/features/quote.html)
* [Bulleted List]({{ site.baseurl }}/features/bulleted-list.html)
* [Numbered List]({{ site.baseurl }}/features/numbered-list.html)
* Emoticons/Emojis

{% endcapture %}

{% capture notes %}

* It is almost impossible to predict every possible type of an article comment, therefore there is no strict set of elements that will be included in the content.

{% endcapture %}

{% capture figures %}

1. <a id="fig-ref1"></a>[Comandeer's comment to the	<i>Image</i> issue inside Editor Recommendations repository](https://github.com/ckeditor/editor-recommendations/issues/14#issuecomment-191782619).

{% endcapture %}

{% include use-case.html %}
