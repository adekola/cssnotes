#Creating Lists

Three types of lists in HTML

* Unordered Lists `<ul></ul>`
* Ordered Lists `<ol></ol>` : has a `start` attribute which determines the the number from which the items should start. It's also possible to reverse
the order of the list by including the `reversed` attribute. 

> Each `<li>` item within a list has a `value` attribute which determines it's value within the list. Subsequent items will continue the numbering from this value.

* Description Lists `<dl><dt></dt><dd></dd></dl>`: for enumerating multiple terms and their descriptions, such as in a glossary.

##List Item Stlying
`list-style-type` property enables one to specify the style of the list item marker to be used with a list. Several possible values exist such as:
* `none`
* `disc`
* `circle`
* `square`
* `decimal`
* `decimal-leading-zero`
* `lower-roman`
* `upper-roman`
* `lower-greek`
* `upper-greek`
* `lower-alpha`
* `upper-alpha`
* `armenian`
* `georgian`

###Using an image as list item marker
Involves removing the default list item marker, by setting `list-style-type: none` and then setting an image in the `background` property and then some padding to the left of the text in the `<li>` to make room for the image.

`list-style-position` - determines the position of the item marker relative to the text. defaults to `outside` which places the marker to the left of the `<li>` element 
and prevents any content from wrapping around it. the `inside` value places the marker in line with the first line of the `<li>` and allows other content to wrap around it

> Shorthand - `list-style: type position`

##Horizontally displaying lists
Simply change the `display` property to `inline` or `inline-block`. This removes the ist item marker. If the item marker is important, `float: left`
the `<li>` instead as well as provide horizontal padding or margin so the marker sits next to the list item.

