---
case:
  title: "Blog/Article"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/9"

layout: default
---

{% capture description %}

It's probably the most common use case for content editor. As such, it defines many features that editor should have to fully allow creating that kind of content.

## Structure

Although not oficially specified, that format follows some strict conventions, which are <i>de facto</i> standard. That conventions are derived from newspapers ones. Therefore blog/article has strong semantic structure, dividing text into logical fragments, denotated frequently by headings.

{% include thumbnail.html src="../images/use_case/blog-article/example-1-thumbnail.png" full="../images/use_case/blog-article/example-1.png" alt="Example of blog article, showing few of most frequently used features: images, headings, paragraphs, links, lists and quotes" caption="<b>Example 1:</b> basic form of blog/article" %}

That example shows how the most common form of blog/article looks alike. It's divided into 4 sections, denotated by subheadings. The hierarchy of content is exposed by using different rank of headers (e.g. "Practical advice" uses `h3` element and therefore is a subsection of "The HTML5 Document Outline is a dangerous fiction" section that uses `h2` element). The sections are also divided internally into paragraphs.

All additional elements (such as images, quotes, lists) are marked using proper, semantic HTML syntax:

* Typical typographic conventions, such as bold or italic, are created using standard HTML elements, such as `strong` or `em`.
* Image is inserted using `img` tag with proper `[alt]` attribute, indicating the role and the meaning of that image in the whole article.
* Links are created using standard HTML element for linking, `a`. Note that text inside links gives the user a descriptive label for the linked content.
* Quotes are created using standard HTML element for quoting bigger ammounts of content, `blockquote`.
* List are created using standard HTML element for marking up unordered lists, `ul`.

There are also some additional features, that can vary across different types of blog/article. In example 1 such a feature is used to display an excerpt from webpage's code in a user friendly way; it uses `pre` element – standard HTML element for preformatted content. The other additional feature is used for marking HTML tags' names inside text, using `code` element – standard HTML element for indicating computer's code.

{% include thumbnail.html src="../images/use_case/blog-article/example-2-thumbnail.png" full="../images/use_case/blog-article/example-2.png" alt="Example of blog article, showing few of most frequently used features: multimedia content, headings, paragraphs, links, lists and quotes" caption="<b>Example 2:</b> additional feature of blog/article – video content" %}

Example 2 presents other very frequently used additional feature: embedding multimedia content inside blog/article. Note that content can be embedded from various sources and using different methods (e.g. by injecting `script` or inserting `iframe`) and can be of any kind ( e.g. images, animated images, audio, video, Flash content).

There is also important that multimedia content can be aligned in a way that not interfere with the flow of the text:

{% include thumbnail.html src="../images/use_case/blog-article/example-3-thumbnail.png" full="../images/use_case/blog-article/example-3.png" alt="Example of right aligned media content (the photos of Saturn V rocket and Earth's surface see from Moon with their captions) inside Wikipedia's article about Apollo 11's mission" caption="<b>Example 3:</b> right aligned images in Wikipedia's article" %}

It is also worth noting that blog/article is not an independent form of content, but it is a part, usually the main one, inside the whole webpage, therefore it should not interfere with semantics of it. The blog/article is dependent of its context of appearance and its own semantic structure must be treated as a part of the semantic structure of the whole webpage. The main concern is rank of headers to create the proper webpage's outline<sup>[[1](#ref1)] [[2](#ref2)]</sup>.

{% include thumbnail.html src="../images/use_case/blog-article/example-4-thumbnail.png" full="../images/use_case/blog-article/example-4.png" alt="Example of webpage with black, floating header at the top, navigational menu for the content on the left, main content (blog/article) on the right and comments and footer under main content" caption="<b>Example 4:</b> the context of blog/article's appearance (blog/article is marked with red border)" %}

## Additional information

* It is almost impossible to predict every possible type of blog/article, therefore there is no strict set of elements that will be included into content.
* Blogs/articles are usually written by people that do not know semantics of HTML (as they are content creators, not webdevelopers), therefore they tend to completely rely on WYSIWYG approach. It is also worth noting that they treat WYSIWYM and WYSIWYG approaches as the same one. In the result many blogs/articles have semantic and/or accessibility problems and could be wrongly understood by people with disabilities who use Assistive Technology or search engines, like Google or Bing.

## Guidelines for editor

* Editor SHOULD deliver set of features, that could be used by the wide variety of blog/articles types, by default.
* If editor is being used for particular type of content, editor MUST be able to deliver needed additional features. Editor MAY do it by a system of plugins.
* Editor MUST implement at least the following set of features:
	* automatically converting new lines into paragraphs to create semantic structure of the content;
	* basic typographic formatting, such as bold or italic;
	* ability to link other resources;
	* way of creating properly ranked headings that would divide content into meaningful parts.
* Editor SHOULD implement following additional features:
	* inserting images with proper textual alternatives;
	* ability to control the position and way of displaying of inserted images;
	* marking quotes using proper HTML syntax;
	* marking lists using proper HTML syntax.
* Editor MAY implement following additional features, depending of the type of content being created:
	* embedding multimedia content, other than images, with appropiate textual alternatives;
	* ability to control the position and way of displaying of embedded multimedia content;
	* additional typographic formatting, such as indicating computer's code;
	* any other additional feature that is likely to be used in type of the content being created.
* Editor MUST produce syntactically valid HTML that is aware of the whole webpage's context. Editor SHOULD encourage user to use semantic, not presentational, markup.
* Editor SHOULD provide a feature, that is usable by people without technical knowledge, to check content for semantic and accessibility problems and a feature that could fix such problems.

## Sources of examples

1. [Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. [Wojtek Cichoń, <i>4 Common CKEditor Installation Mistakes And How To Avoid Them</i>](http://ckeditor.com/blog/4-Common-CKEditor-Installation-Mistakes-And-How-To-Avoid-Them).
3. [<i>Apollo 11</i>](https://en.wikipedia.org/wiki/Apollo_11).
4. [Comandeer, <i>Data po polsku</i>](http://tutorials.comandeer.pl/js-intl.html).

## References

1. <a id="ref1"></a>[Steve Faulkner, <i>The HTML5 Document Outline</i>](https://www.paciellogroup.com/blog/2013/10/html5-document-outline/).
2. <a id="ref2"></a>[G141: Organizing a page using headings](http://www.w3.org/TR/WCAG20-TECHS/<G141 class="html"></G141>).

{% endcapture %}

{% include use-case.html %}
