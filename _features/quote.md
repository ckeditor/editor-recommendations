---
feature:
  name: "Quote"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/18"

layout: default
---

{% capture description %}

The **Quote** feature provides the user with the ability to insert a self-contained quote, that can be referenced from edited content.

The quote is usually accompanied with a source reference.

{% endcapture %}

{% capture ui %}

 * UI: A feature inserting the proper quote element into the editor's editable area, usually represented as a button with the "<i class="fa fa-quote-right" aria-label="Quote" title="Quote"></i>" icon
 * Title: "Quote"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<figure>` element MUST be used to represent the **Quote** feature as it is the standard way to express self-contained non-textual additional content<sup>[[1](#ref1)]</sup>.

The `<figure>` element SHOULD have a `class` attribute which value is set to `quote` to identify that the element is being used for representing quote and to allow styling that particular use-case.

The `<blockquote>` element MUST be used to represent the quote itself as it is the standard way to express a quote in HTML<sup>[[2](#ref2)]</sup>.

The `<blockqoute>` element MAY have `cite` attribute<sup>[[3](#ref3)]</sup>, containing a valid URL<sup>[[4](#ref4)]</sup> pointing to the source of citation.

The name of the source of citation, if it is present, MUST be represented by the `<cite>` element<sup>[[5](#ref5)]</sup> nested inside `<figcaption>` element<sup>[[6](#ref6)]</sup>. If the name of the source is not present, the `<figcaption>` element MAY be used to provide a caption for the quote.

Example:

```html
<figure class="quote">
	<blockquote cite="https://pl.wikisource.org/wiki/Pan_Tadeusz_(wyd._1834)/Ksi%C4%99ga_pierwsza">
		<p>Litwo! Ojczyzno moja! ty jesteś jak zdrowie.<br>
		Ile cię trzeba cenić, ten tylko się dowie,<br>
		Kto cię stracił. Dziś piękność twą w całej ozdobie<br>
		Widzę i opisuję, bo tęsknię po tobie.</p>
	</blockquote>
	<figcaption><cite>Adam Mickiewicz, <i>Pan Tadeusz</i></cite></figcaption>
</figure>
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<figure>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element).
2. <a id="ref2"></a>[The `<blockquote>` element definition in the HTML 5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element).
3. <a id="ref3"></a>[The `cite` attribute definition in the HTML 5 standard](https://www.w3.org/TR/html5/grouping-content.html#attr-blockquote-cite).
4. <a id="ref4"></a>[The definition of a valid URL in the HTML 5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls).
5. <a id="ref5"></a>[The `<cite>` element definition in the HTML 5 standard](https://www.w3.org/TR/html5/text-level-semantics.html#the-cite-element).
6. <a id="ref6"></a>[The `<figcaption>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element).

{% endcapture %}

{% include feature.html %}
