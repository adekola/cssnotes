#Backgrounds and Gradients

Backgrounds play an important role in the aesthetics of web pages and so deserve some forethought and deliberation.

###Properties
* `background-color` or `background` :  sets a solid color or a color/image respectively.

> To use transparent values (HSBa and RGBa), keep in mind to provide fallbacks so that browsers that don's support transparent color values can use the ones they do undertsand - hex and color keywords. Do this by sepcifying two background-color properties; the safe one above, and the funky one below. (to take advantage of CSS cascading).

* `background-image: url('path/to/image')`:  sets the image to use for the background.
* `background-repeat: repeat, repeat-x, repeat-y, no-repeat`:  sets the option to reapt or not for the background image.
* `background-position: 0px 0px`:  sets the position for the background image, defined by horizontal and vertical (respectively) offset to the left top corner. Keyword values can also be used to specify the position - `left top bottom right`, in different combinations.

####Background Property Shorthand Values
When specified in shorthand, `background` can be specfied in the order `background-color, background-image, background-position, background-repeat`.

###Linear Gradients
Achieved by using the `linear-gradient(direction, start-color, end-color)` function. The browser handles the transition between both colors. It's good practise to include a solid background color in case the accessing browser doesn't support linera gradients. The first parameter which is the direction is specified by a combination of key word value `top bottom left right`. E.g. `to right bottom`. Degree values are also acceptable. e.g 135 for bottom right.

###Radial Gradients
To specify a radial gradient background, one would use the `radial-gradient(start-color, end-color)` function as the value for a `background` or `background-image` property. These gradients work from the inside to the outside of the element. Starting with the  start color and ending with the end color.

**Gradient Color Stops**
> It is equally possible to assign color stops for the linear gradient to create transitons between more than 2 colors.

###Multiple Background Images
By chaining the definition of background properties, several images can be used. Like so:
`background:  url("foreground.png") 0 0 no-repeat, url("middle-ground.png") 0 0 no-repeat, url("background.png") 0 0 no-repeat;`

###New Background properties
Starting in CSS3, three new props were introduced 
* `background-size`:  if % values are used, they denote % of the elements size or width resepctively. Keyword value `auto` can be used to maintain the aspect ratio of the image.
> `cover` and `contain` key word values may be used for the `background-size` property to indicate that the image should be resized to cover the element entirely (shrink or stretched). It may cut out some elements of the original image. `contain` specifies that he image be resized to remain entirely contained within the holdign element. `contain` will always show the entire image within the element, tho it may not completely cover it.

*  `background-clip`: specifies the surface area which the image should cover. (defaults to `border-box`)
*  `background-origin`: specifies where the `background-position` should start. (defaults to `padding-box`)
Both properties accept values of `border-box`, `padding-box` or `content-box`.



