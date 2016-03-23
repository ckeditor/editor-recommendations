---
feature:
  name: "Image"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/14"

layout: default
---

{% capture description %}

The **Image** feature provides the user with the ability to insert a self-contained image, that can be referenced from edited content.

The image is usually accompanied with a caption.

{% endcapture %}

{% capture ui %}

 * UI: A feature providing the user with a way to set the properties of a new image, usually represented as a button with the "<i class="fa fa-image" aria-label="Image" title="Image"></i>" icon that opens a dialog with form fields to edit image properties
 * Title: "Image"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<figure>` element MUST be used to represent the **Image** feature as it is the standard way to express self-contained non-textual additional content<sup>[[1](#ref1)]</sup>.

The `<figure>` element SHOULD have a `class` attribute which value is set to `image` to identify that the element is being used for representing image and to allow styling that particular use-case.

The `<img>` element MUST be used to represent the image itself as it is the standard way to express an image in HTML<sup>[[2](#ref2)]</sup>.

The `<img>` element MUST have at least the following attributes:

* The `[src]` attribute with a valid URL pointing to the image<sup>[[3](#ref3)]</sup>.
* The `[alt]` attribute that contains the textual alternative for the image, if any, or is empty, if the image conveys the information that could be derived from its context or caption<sup>[[4](#ref4)]</sup>.

The caption, if it is present, MUST be represented by the `<figcaption>` element<sup>[[5](#ref5)]</sup>.

Example:

```html
<figure class="image">
	<img src="http://c.cksource.com/a/1/img/sample.jpg" alt="Saturn V carrying Apollo 11">
	<figcaption>Figure 1: Beginning of Apollo 11 mission</figcaption>
</figure>
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<figure>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element).
2. <a id="ref2"></a>[The `<img>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element).
3. <a id="ref3"></a>[The definition of a valid URL in the HTML5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls).
4. <a id="ref4"></a>[Requirements for providing text to act as an alternative for images in the HTML5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#alt).
5. <a id="ref5"></a>[The `<figcaption>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element).

{% endcapture %}

{% include feature.html %}
