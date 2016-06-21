---
feature:
  name: "Table"
  description: Draft for Table feature in WYSIWYG.
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/44"

layout: default
---

{% capture description %}

The **Table** feature allows the user to create data table.

{% endcapture %}

{% capture ui %}

 * UI: A feature providing the user with a way to set up properties for the new table, usually represented as a button with the "<i class="fa fa-table" title="Table" aria-hidden="true"></i><span class="sr-only">Table</span>" icon that opens a dialog window with form fields to edit the table properties
 * Title: "Table"
 * Keystroke: –

{% endcapture %}

{% capture markup %}

The `<figure>` element MUST be used to represent the **Table** feature as it is the standard way to express self-contained non-textual additional content<sup>[[1](#ref1)]</sup>.

The `<figure>` element SHOULD have a `class` attribute which value is set to `table` to identify that the element is being used for representing table and to allow styling that particular use-case.

The `<table>` element MUST be used to represent the table itself as it is the standard way to express a table in HTML<sup>[[2](#ref2)]</sup>.

The `<table>` SHOULD have a header placed inside `<thead>` element<sup>[[3](#ref3)]</sup>. If the `<thead>` element is not present, the first row of the table MUST represent the header<sup>[[4](#ref4)]</sup>. The header MUST contain a row with headings for each column, represented by `<tr>` element with `<th>` elements inside<sup>[[5](#ref5), [6](#ref6)]</sup>. The `<th>` elements MAY have `scope` attribute with value set to `col`<sup>[[7](#ref7)]</sup>.

The contents of the table SHOULD be placed inside `<tbody>` element<sup>[[8](#ref8)]</sup>. The content MUST be divided into rows, represented by `<tr>` elements, and rows MUST be divided into cells, represented by `<td>` elements<sup>[[4](#ref4), [9](#ref9)]</sup>.

The caption for the table, if it is present, MUST be placed inside `<figcaption>` element<sup>[[10](#ref10)]</sup>.

Example:

```html
<figure class="table">
    <table>
        <thead>
            <tr>
                <th scope="col">Person</th>
                <th scope="col">Position</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>John Smith</td>
                <td>JS developer</td>
            </tr>
            <tr>
                <td>John Doe</td>
                <td>Java developer</td>
            </tr>
            <tr>
                <td>John DeFoe</td>
                <td>ASP .NET developer</td>
            </tr>
        </tbody>
    </table>
    <figcaption>Company's most valuable employees</figcaption>
</figure>
```

{% endcapture %}

{% capture references %}

1. <a id="ref1"></a>[The `<figure>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element).
2. <a id="ref1"></a>[The `<table>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-table-element).
3. <a id="ref3"></a>[The `<thead> element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-thead-element).
4. <a id="ref4"></a>[<i>Techniques for WCAG 2.0. H51: Using table markup to present tabular information</i>](https://www.w3.org/TR/WCAG20-TECHS/H51.html).
5. <a id="ref5"></a>[The `<tr>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-tr-element).
6. <a id="ref6"></a>[The `<th>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-th-element).
7. <a id="ref7"></a>[The `scope` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#attr-th-scope).
8. <a id="ref8"></a>[The `<tbody>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-tbody-element).
9. <a id="ref9"></a>[The `<td>` element definition in the HTML5 standard](https://www.w3.org/TR/html5/tabular-data.html#the-td-element).
10. <a id="ref10"></a>[The `<figcaption>` element definition in the HTML5 standard](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element).

{% endcapture %}

{% include feature.html %}
