---
case:
  title: "Blog/Article"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/9"

layout: default
---

{% capture description %}
Although not oficially specified, that format follows some strict conventions, which are <i>de facto</i> standard. That conventions are derived from newspapers ones. Therefore blog/article has strong semantic structure, dividing text into logical fragments, denotated frequently by headings. The textual content is usually accompanied by multimedia content, especially images.

{% include thumbnail.html src="use_case/blog-article/fig-1-thumbnail.png" full="use_case/blog-article/fig-1.png" alt="Example of blog article, showing few of most frequently used features: images, headings, paragraphs, links, lists and quotes" caption="<b>Fig. 1:</b> basic form of blog/article" %}

{% endcapture %}


{% capture features %}

* Heading
* [Link]({{ site.baseurl }}/features/link.html)
* [Bold]({{ site.baseurl }}/features/bold.html)
* [Italic]({{ site.baseurl }}/features/italic.html)
* [Strikethrough]({{ site.baseurl }}/features/strikethrough.html)
* [Image]({{ site.baseurl }}/features/image.html)
* Quote
* [Bulleted List]({{ site.baseurl }}/features/bulleted-list.html)
* [Numbered List]({{ site.baseurl }}/features/numbered-list.html)


{% endcapture %}

{% capture usability %}

* [Auto-paragraphing]({{ site.baseurl }}/usability/enter.html#auto-paragraphing)

{% endcapture %}

{% capture notes %}

* It is almost impossible to predict every possible type of blog/article, therefore there is no strict set of elements that will be included into content.
* It is worth noting that blog/article is not an independent form of content, but it is a part, usually the main one, inside the whole webpage, therefore it should not interfere with semantics of it. The blog/article is dependent of its context of appearance and its own semantic structure must be treated as a part of the semantic structure of the whole webpage. The main concern is rank of headers to create the proper webpage's outline<sup>[[1](#ref1)] [[2](#ref2)]</sup>.

{% include thumbnail.html src="use_case/blog-article/fig-2-thumbnail.png" full="use_case/blog-article/fig-2.png" alt="Example of webpage with black, floating header at the top, navigational menu for the content on the left, main content (blog/article) on the right and comments and footer under main content" caption="<b>Fig. 2:</b> the context of blog/article's appearance (blog/article is marked with red border)" %}

* Blogs/articles are usually written by people that do not know semantics of HTML (as they are content creators, not webdevelopers), therefore they tend to completely rely on WYSIWYG approach. It is also worth noting that they treat WYSIWYM and WYSIWYG approaches as the same one. In the result many blogs/articles have semantic and/or accessibility problems and could be wrongly understood by people with disabilities who use Assistive Technology or search engines, like Google or Bing. Therefore there is a need for a simple tool that will check markup and report all semantic and accessibility errors<sup>[[3](#ref3)]</sup>.

{% endcapture %}

{% capture images %}

1. [Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. [Comandeer, <i>Data po polsku</i>](http://tutorials.comandeer.pl/js-intl.html).

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. <a id="ref2"></a>[<i>G141: Organizing a page using headings</i>](http://www.w3.org/TR/WCAG20-TECHS/<G141 class="html"></G141>).
3. <a id="ref3"></a>[<i>About Accessibility Checker</i>](https://cksource.com/a11ychecker/demo/about.html).

{% endcapture %}

{% include use-case.html %}
