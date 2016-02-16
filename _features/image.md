---
feature:
  name: "Image"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/14"

layout: default
---

{% capture description %}

The **Image** feature provides the user with the ability to insert an image into edited content.

{% endcapture %}

{% capture ui %}

 * UI: A feature providing the user with a way to set the properties of a new image, usually represented as a button with the "<i class="fa fa-image" aria-label="Image" title="Image"></i>" icon that opens a dialog with form fields to edit image properties
 * Title: "Image"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<img>` element MUST be used to represent the **Image** feature as it is the standard way to express an image in HTML<sup>[[1](#ref1)]</sup>.

The image element MUST have at least the following attributes:

* The `[src`] attribute with a valid URL pointing to the image<sup>[[2](#ref2)]</sup>.
* The `[alt]` attribute that contains the textual alternative for the image, if any, or is empty if the image purpose is purely decorative<sup>[[3](#ref3)]</sup>.

Example:

```
<img src="http://c.cksource.com/a/1/img/sample.jpg" alt="Saturn V carrying Apollo 11">
```

{% endcapture %}

{% capture implementation %}

* If the image is intended to be displayed on a wide variety of devices, it SHOULD be declaratively (as part of created content) marked as responsive. This could be achieved by using one of the following methods<sup>[[4](#ref4), [5](#ref5)]</sup>:
	* The `[srcset]` attribute added to the `<img>` element<sup>[[1](#ref1)]</sup>.
	* The `<picture>` element<sup>[[6](#ref6)]</sup>.
* Additional semantic value for images MAY be provided by using the `<figure>` and `<figcaption>` elements<sup>[[7](#ref7), [8](#ref8)]</sup>.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<img>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element)
2. <a id="ref2"></a>[The definition of a valid URL in the HTML 5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls)
3. <a id="ref3"></a>[Requirements for providing text to act as an alternative for images in the HTML5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#alt)
4. <a id="ref4"></a>[<i>Use Cases and Requirements for Standardizing Responsive Images</i>](http://usecases.responsiveimages.org/)
5. <a id="ref5"></a>[Adaptive images in the HTML5 standard](http://www.w3.org/TR/html51/semantics.html#adaptive-images)
6. <a id="ref6"></a>[The `picture` element definition in the HTML 5.1 draft](http://www.w3.org/TR/html51/semantics.html#the-picture-element)
7. <a id="ref7"></a>[The `<figure>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element)
8. <a id="ref8"></a>[The `<figcaption>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element)

{% endcapture %}

{% include feature.html %}
