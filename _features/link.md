---
feature:
  name: "Link"
  description: Draft for Link feature in WYSIWYG.
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/10"

layout: default
---

{% capture description %}

The **Link** feature provides the user with the ability to link some parts of content to other web resources or other parts of the same content. This feature inserts a new link with a specified text or transforms the selected, previously existing text into a link.

{% endcapture %}

{% capture ui %}

 * UI: A feature providing the user with a way to set up properties for the new link, usually represented as a button with the "<i class="fa fa-link" title="Link" aria-hidden="true"></i><span class="sr-only">Link</span>" icon that opens a dialog window with form fields to edit the link properties
 * Title: "Link"
 * Keystroke: <kbd>Ctrl+K</kbd>

{% endcapture %}

{% capture markup %}

The `<a>` element MUST be used to represent the **Link** feature as it is the standard way to express links in HTML<sup>[[1](#ref1)]</sup>.

The link element MUST have at least the `[href]` attribute whose value is a valid URL<sup>[[2](#ref2)]</sup>.

The link element MAY have other attributes defined for the HTML `<a>` element, such as `[target]`, `[download]`, `[rel]` or `[hreflang]`<sup>[[1](#ref1)]</sup>.

Example:

```html
<a href="http://ckeditor.com">CKEditor</a> is an online rich text editor.
```

{% endcapture %}

{% capture implementation %}

* In offline text editors, such as Microsoft Word or LibreOffice Writer, a keystroke for inserting a link is <kbd>Ctrl+K</kbd> and this keystroke is a _de facto_ standard for inserting links. However it should be noted that this keystroke is reserved in web browsers and reassigning it may cause issues with user experience<sup>[[3](#ref3)]</sup>.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<a>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element).
2. <a id="ref2"></a>[The definition of a valid URL in the HTML5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls).
3. <a id="ref3"></a>[A message about the <kbd>Ctrl+K</kbd> keystroke in browsers in a discussion about a keystroke for inserting links in GMail](https://productforums.google.com/d/msg/gmail/np9xeA97kBk/HSWwZFnDHS0J).

{% endcapture %}

{% include feature.html %}
