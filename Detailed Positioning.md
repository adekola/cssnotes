#Detailed Positioning
At times, one needs to adopt other strategies for positioning aside from `float`ing elements. Relative or absolute postioning may be more appropriate in certain
contexts. Let's see what's possible.

##Containing Floats
When floated, an element's position depends on the other elements which are positioned around it. It allows elements to interact with one another based on their
size and the size of their containing parent.

> A common problem with floats is obvious when for instance, a parent element contains many floated children. In this case, the parent loses sight of what it contains and reduces to having a ``height` of `0` and ignoring several other properties
Though not often noticed, it's quite a problem, but in fact it causes the children elements to no longer impact the outer borders of the parent.

A few techniques to effectively contain floats. They include:
###Overflow
Setting the `overflow` property to `auto` will contain the floats and result in an actual height for the parent element.
> This has a drawback though. It could make elements which extend outside of the parent to be cut of abruptly. BEsides, some browsers will render the 
target element with scrollbars which may not be your intention.

###Clearfix
A bit more complex, but it has more consistent support across browsers. It is based on the using the `:before` and `:after` pseudo elements ont the parent element.
Usually looks like this, where `group` is a class for parent elements which will contain floated children

```
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  *zoom: 1;
}

```

##Position Property
For cases where you need more control over the position of an element than is provded by `float`, you can use the `position` property. It has five different values with their unique effects on the position of an element.

* `static` - the default value of the property for elements, meaning they don't have and will not accept box offset properties.
* `relative` - accepts the box offset properties `top`, `bottom`, `left` and `right`. The values of this properteis determine how the element shoudl be positioned relative to it's default position.
it's important to note that this stil leaves the element in it's default position on the page i.e.othr elements can not come into it's carved out position on the page.
Moreso, such an element may overlap or underlap other elements without moving them from their position. 
> if both the `top` and `bottom` properties are declared for an elemtn , the `top` property takes prioritiy. If both `left` and `right` propeties are declared, the 
priority is given to the direction of the language in which the page is written. e.g. `left` for English and `right` for Arabic.

* `absolute` - this value has the effect of removing the element from the flow of the page and positioning it relative to it's nearest relatively positioned 
element. If there is no such element, it is positioned relative to the `body` element.

* `fixed` - similar to `absolute`, only this time, it fixed in relation to the browser viewport and so doesn't scroll with the page.
To use this for footers for example, be sure to set the `left` and `right` offsets to `0` 
_ This CSS value doesn't work with IE6 though_


##Z-index
This property allows us to stack elements on each other visually. Generally, elements are positioned on the z-axis in the order in which they appear in the DOM. 
Elements at the top of the DOM are positioned behind elements coming after. The `z-index` property allows us to change this. To use this property, a position 
value of `absolute`, `fixed` or `relative`. The element with the highest `z-index` is shown above all others.
