---
feature:
  name: "Image"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/14"

layout: default
---

{% capture description %}

The **Image** feature provides user the ability to link some parts of content to other web resources or other parts of the same content by inserting link with specified text or by transforming existing, selected text into link.

{% endcapture %}

{% capture ui %}

 * UI: feature providing user a way to set up properties for the new image, usually represented as button with "<i class="glyphicon glyphicon-picture" aria-label="Image" title="Image"></i>" icon that opens dialog containing form fields to edit image's properties
 * Title: "Image"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `img` element MUST be used to represent the **Image** feature as it is the standard way to express image in HTML<sup>[[1](#ref1)]</sup>.

Image element MUST have at least `[src`] attribute, that is a valid URL pointing to image<sup>[[2](#ref2)]</sup>, and`[alt]` attribute, that contains the textual alternative for the image, if any, or is empty if the image's purpose is purely decorative<sup>[[3](#ref3)]</sup>.

Example:

```
<img src="http://c.cksource.com/a/1/img/sample.jpg" alt="Saturn V carrying Apollo 11">
```

{% endcapture %}

{% capture implementation %}

* If the image is intended to be displayed on wide variety of devices, it SHOULD be declaratively (as part of created content) marked as responsive. It could be achieved by using one of two methods<sup>[[4](#ref4), [5](#ref5)]</sup>:
	* `[srcset]` attribute added to `img` element<sup>[[1](#ref1)]</sup>,
	* `picture` element<sup>[[6](#ref6)]</sup>.
* Additional semantic value for images MAY be provided by using `figure` and `figcaption` elements<sup>[[7](#ref7), [8](#ref8)]</sup>.

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[`img` element definition in HTML 5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element)
2. <a id="ref2"></a>[Definition of valid URL in HTML 5 standard](http://www.w3.org/TR/html5/infrastructure.html#urls)
3. <a id="ref3"></a>[Requirements for providing text to act as an alternative for images in HTML5 standard](http://www.w3.org/TR/html5/embedded-content-0.html#alt)
4. <a id="ref4"></a>[<i>Use Cases and Requirements for Standardizing Responsive Images</i>](http://usecases.responsiveimages.org/)
5. <a id="ref5"></a>[Adaptive images in HTML5 standard](http://www.w3.org/TR/html51/semantics.html#adaptive-images)
6. <a id="ref6"></a>[`picture` element definition in HTML 5.1 draft](http://www.w3.org/TR/html51/semantics.html#the-picture-element)
7. <a id="ref7"></a>[`figure` element definition in HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element)
8. <a id="ref8"></a>[`figcaption` element definition in HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element)

{% endcapture %}

{% include feature.html %}
