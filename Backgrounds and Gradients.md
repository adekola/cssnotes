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
To specify a radial gradient background, one would use the `radial-gradient(start-color, end-color)` function as the value for a `background` or `background-image` property. These gradients work from the inside to the outsude of the element. Starting with the  start color and ending with the end color.

**Gradient Color Stops**
> It is equally possible to assign color stops for the linear gradient to create transitons between more than 2 colors.





