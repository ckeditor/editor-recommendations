---
feature:
  name: "Link"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/10"

layout: default
---

{% capture description %}

The **Link** feature provides user the ability to link some parts of content to other web resources or other parts of the same content by inserting link with specified text or by transforming existing, selected text into link.

{% endcapture %}

{% capture ui %}

 * UI: feature providing user a way to set up properties for the new link, usually represented as button with "<i class="glyphicon glyphicon-link" aria-label="Link" title="Link"></i>" icon that opens dialog containing form fields to edit link's properties
 * Title: "Link"
 * Keystroke: <kbd>CTRL+L</kbd>

{% endcapture %}

{% capture markup %}

The `a` element MUST be used to represent the **Link** feature as it is the standard way to express link in HTML<sup>[[1](#ref1)]</sup>.

Link element MUST have at least `[href]` attribute which value is a valid URL<sup>[[2](#ref2)]</sup>.

Link element MAY have other attributes defined for HTML `a` element, such as `[target]`, `[download]`, `[rel]` or `[hreflang]`<sup>[[1](#ref1)]</sup>.

Example:

```
<a href="http://ckeditor.com">CKEditor</a> is an online rich-text editor.
```

{% endcapture %}

{% capture implementation %}

* In offline text editors, such as Microsoft Word or LibreOffice Writer, keystroke for inserting link is <kbd>CTRL+K</kbd>, but that keystroke is reserved in browsers and SHOULD NOT be altered<sup>[[3](#ref3)]</sup>.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`a` element definition in HTML5 standard](http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element)
2. <a id="ref2"></a>[Definition of valid URL in HTML5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls)
3. <a id="ref3"></a>[Message about <kbd>CTRL+K</kbd> keystroke in browsers in discussion about keystroke for inserting links in GMail](https://productforums.google.com/d/msg/gmail/np9xeA97kBk/HSWwZFnDHS0J)

{% endcapture %}

{% include feature.html %}
