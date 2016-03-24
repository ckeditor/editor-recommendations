---
case:
  title: "Blog/Article"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/9"

layout: default
---

{% capture description %}
Although not oficially specified, this format follows some strict conventions which are <i>de facto</i> standard. These conventions are derived from newspapers ones. A blog/article has a strong semantic structure that divides the text into logical fragments and is frequently denoted  by headings. The textual content is usually accompanied with multimedia content, especially images.

{% include figures/thumbnail.html src="use_case/blog-article/fig-1-thumbnail.png" full="use_case/blog-article/fig-1.png" alt="An example of a blog article, showing a few of the most frequently used features: images, headings, paragraphs, links, lists and quotes" caption="A basic form of a blog/article." %}

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

* [Auto-paragraphing]({{ site.baseurl }}/usability/enter-key.html#auto-paragraphing)

{% endcapture %}

{% capture notes %}

* It is almost impossible to predict every possible type of a blog/article, therefore there is no strict set of elements that will be included in the content.
* A blog/article is not an independent form of content, but it is a part (usually the main one) of an entire webpage. As a result,  it should not interfere with the webpage semantics. A blog/article is dependent on its context of appearance and its own semantic structure must be treated as a part of the semantic structure of the whole webpage. The main concern is the rank of headers to create the proper webpage outline<sup>[[1](#ref1)] [[2](#ref2)]</sup>.

{% include figures/thumbnail.html src="use_case/blog-article/fig-2-thumbnail.png" full="use_case/blog-article/fig-2.png" alt="An example of a webpage with a black, floating header at the top, navigational menu for the content on the left, main content (blog/article) on the right and comments and footer under main content" caption="The context of a blog/article's appearance (blog/article is marked with a red border)." %}

* Blogs/articles are usually written by people that do not know the semantics of HTML (as they are content creators, not web developers), therefore they tend to completely rely on the WYSIWYG approach. Content creators often treat WYSIWYM and WYSIWYG approaches as the same. As a result many blogs/articles have semantic and/or accessibility problems and could be misunderstood by people with disabilities who use Assistive Technology or by search engines, like Google or Bing. There is thus a need for a simple tool that will check the markup and report all semantic and accessibility errors<sup>[[3](#ref3)]</sup>.

{% endcapture %}

{% capture figures %}

1. <a id="fig-ref1"></a>[Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. <a id="fig-ref2"></a>[Comandeer, <i>Data po polsku</i>](http://tutorials.comandeer.pl/js-intl.html).

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. <a id="ref2"></a>[<i>G141: Organizing a page using headings</i>](http://www.w3.org/TR/WCAG20-TECHS/<G141 class="html"></G141>).
3. <a id="ref3"></a>[<i>About Accessibility Checker</i>](https://cksource.com/a11ychecker/demo/about.html).

{% endcapture %}

{% include use-case.html %}
