#Complex Selectors

In CSS3 , selectros got the attention they so much deserved as they're one of the most important aspects of CSS, affecting the casacade as well as the elemtns and amanner in which stles are applied.

##Common Selectors
* **type** - these identify an element by it's type in the HTML spec. Think about `body`, `h1` etc.
* **class** - identifies an element by it's class attribute, which can be appleid to sevral elements within the same page.
* **id** - these identify an element by it's id attribute. This attribute isunique and should only be used once within a page.


##Child Selectors
For selecting elemants which fall inside another, thus making them a child of another element.

###Descedant Selectors
This selects elements which fall under an ancestor element. It doesn't have to be an immediate descendant (i.e. a child) of the ancestor. This takes the form:
`section div {  }` for example. Specified with a spacing between the two elements.

###Direct child Selectors
This selects only descedeants which are direct children of the ancestor. Specified with a `>` between the related elements.

##Sibling Selectors
To select elements which share a common parent. 

###General Sibling Selectors
To select elements which follow each other and share a common parent. e.g. `h2 ~ p` will select `p` elements which follow `h2` elements anywhere and share the same parent.

###Adjacent Sibling Selectors
To select sibling elements directly next to each other. e.g. `h2 + p` will select `p` elements which **directly** follow `h2` elements and share the same parent.

##Attribute Selectors
Selecting elements based on the presence or value of their `class` or `id` attributes.

##Attribute Present Selector
This selects an element based on whether an attribute is present or not, regardless of it's actual value. Simply include the name of the target attribute in `[]`.
e.g. `a[target] {}`

##Attribute Value Selector
This is particular about the value of the attribute and not just it's presence. Include the target value of the attribute in `[]` with an `=`. 
e.g `a[href="fb.com"] {}`

##Attribute Contains Selector
This selects an element based on some part of an attribute value, but not an exact match. Include the target value of the attribute in `[]` with an `*`. 
e.g `a[href*="login"] {}`

##Attribute Begins with Selector
`a[href^="login"] {}`

##Attribute Ends with Selector
`a[href$=".pdf"] {}`

##Attribute Spaced Selector
`a[href~="tag"] {}`





