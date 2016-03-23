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
	<blockquote cite="https://en.wikipedia.org/wiki/Apollo_11">
		<p>Apollo 11 was the first spaceflight that landed humans on the Moon. Americans Neil Armstrong and Buzz Aldrin landed on July 20, 1969, at 20:18 UTC (46 years ago). Armstrong became the first to step onto the lunar surface six hours later on July 21 at 02:56 UTC. Armstrong spent about two and a half hours outside the spacecraft, and together with Aldrin collected 47.5 pounds (21.5 kg) of lunar material for return to Earth. The third member of the mission, Michael Collins, piloted the command spacecraft alone in lunar orbit until Armstrong and Aldrin returned to it just under a day later for the trip back to Earth.</p>
	</blockquote>
	<figcaption><cite><i>Apollo 11</i>, Wikipedia.org</cite></figcaption>
</figure>
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<figure>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element).
2. <a id="ref2"></a>[The `<blockquote>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element).
3. <a id="ref3"></a>[The `cite` attribute definition in the HTML5 standard](https://www.w3.org/TR/html5/grouping-content.html#attr-blockquote-cite).
4. <a id="ref4"></a>[The definition of a valid URL in the HTML5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls).
5. <a id="ref5"></a>[The `<cite>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/text-level-semantics.html#the-cite-element).
6. <a id="ref6"></a>[The `<figcaption>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element).

{% endcapture %}

{% include feature.html %}
