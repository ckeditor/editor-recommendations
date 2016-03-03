---
feature:
  name: "Widget"
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/20"

layout: default
---

{% capture description %}

The **Widget** feature indicates the additional content to the main content of the page.

The additional content conveys auxiliary information and is self-contained or even independent from the main content. It is also possible to reference the additional content in the text and move it away from the main content.

The additional content is usually accompanied with the caption.

{% endcapture %}

{% capture subfeatures %}

* [Image]({{ site.baseurl }}/features/image.html)
* Quote

{% endcapture %}

{% capture ui %}

This feature does not define the UI.

{% endcapture %}

{% capture markup %}

The `<figure>` element MUST be used to represent the **Widget** feature as it is the standard way to express self-contained additional content<sup>[[1](#ref1)]</sup>.

The caption, if it is present, MUST be represented by the `<figcaption>` element<sup>[[2](#ref2)]</sup>.

Example 1:

```
<figure>
	<img src="example.png" alt="Image used in the example">
	<figcaption>The caption to the image used in the example.</figcaption>
</figure>
```

Example 2:

```
<figure>
	<table>
		<thead>
			<tr>
				<th scope="col">Toy</th>
				<th scope="col">Manufacturer</th>
				<th scope="col">Price</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<th scope="row">Teddy bear</th>
				<td>Teddy Bear Inc.</td>
				<td>$69</td>
			</tr>
			<tr>
				<th scope="row">Creepy doll</th>
				<td>Teddy Bear Inc.</td>
				<td>$111</td>
			</tr>
		</tbody>
	</table>
	<figcaption>Table #1: Toys with their prices.</figcaption>
</figure>
```

{% endcapture %}

{% capture notes %}

This feature is intended to act as a base for more specialised features, such as Image or Quote, and SHOULD NOT be used directly in the editor. 

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<figure>` element definition in the HTML 5 standard](https://www.w3.org/TR/html5/grouping-content.html#the-figure-element).
2. <a id="ref2"></a>[The `<figcaption>` element definition in the HTML 5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element).

{% endcapture %}

{% include feature.html %}
