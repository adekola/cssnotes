# Working with Typography

##Typeface vs Font
A _typeface_ is what you see, how the text looks, feels and reads.
A _font_ on the other hand is a file which contains a typeface. It is a font that allows the computer to access a typeface. A useful analogy is to think of 
a font as a CD and typeface as a song. Font is what you use, Typeface is what you see or experience.

In building a website, the two most important factors affecting the look and legibility of the website are: **typeface** and **text color**

CSS offers _**font-based properties**_ as well as _**text-based_ properties**_

###Font-based properties
* `font-family` 
* `font-size`
* `font-family` - `italic, normal, oblique, inherit`.
* `font-variant` - to switch text to small capitals which is sometimes required. Values include `normal, small-caps, inherit`.
* `font-weight` - to change the weight of a typeface. Values include `normal, bold, bolder, lighter, inherit`. Numeric values are especially suited for typefaces with multiple weights, starting from 100 (thinnest) to 900 (thickest).

_if you specify a font weight with a value not supported by the typeface, it will default to the closest supported weight_

* `line-height` - the distance between 2 lines of text (also known as leading). The best practise for legibility is to set the `line-height` to 1 or 1.5 times the `font-size` property

**Trick**
> Using the same value for `height` and `line-height` produces the effect of vertically centering the text. Commonly used for `button`s

> The `font`shorthand property can be used to specify the above listed properties in one go.
> `font: font-style, font-variant, font-weight, font-size, line-height, and font-family` like so:
> 
```
html {
  font: italic small-caps bold 14px/22px "Helvetica Neue", Helvetica, Arial, sans-serif;
}
``` 

Note the / between `font-size` and `line-height`. In this shorthand form only the `font-size` and `font-family` properties are mandatory.

**Pseudo-classes**
> Kewords which may be added to the end of a selector to style an element when it is in a unique state. 
> e.g `a:hover { color: #263526; }`

###Text-based properties
Defining `font`y properties is only half the challenge. It's equally important to define properties related to text: alignment, spacing etc.

* `text-align: left, right, center, justify, and inherit`.
* `text-decoration: none, underline, overline, line-through, and inherit` - options to spice up the appearance of text.
* `text-indent` - indents text in elements such as is common for paragraphs in printed publications. +ve values push forward, -ve values push backwards.
* `text-shadow` - enables you to add shadow(s) to text. Accepts four values: _horizontal offset_, _vertical offset_, _blur radius_ and _color_

**Aside**
> while `text-shadow` places a shadow on text, `box-shadow` places a shadow on the entire element and accepts the same values as text-shadow.

* `text-transform: none, capitalize, uppercase, lowercase, and inherit` - transforms the text in-line. Unlike `font-variant` which looks for an alternative variant of a typeface, `text-transform` doesn't.

* `letter-spacing` - adjusts the spacing (or tracking) between letters on a page. A -ve value bring the letter closer while a +ve value pushes them apart.

* `word-spacing` - adjusts the spacing between words on a page. A -ve value bring the letter closer while a +ve value pushes them apart.

##Web Safe fonts
These are fonts which are preinstalled on every computer, phone, tablet or device with capability to browse the internet. They include:

* Arial
* Courier New, Courier
* Garamond
* Georgia
* Lucida Sans, Lucida Grande, Lucida
* Palatino Linotype
* Tahoma
* Times New Roman, Times
* Trebuchet
* Verdana

###Embedding Web Fonts
It's entirely possible to host fonts at an online location and reference them from our CSS using the `font-face` at rule, like so:

```
@font-face {
  font-family: "Lobster";
  src: local("Lobster"), url("lobster.woff") format("woff");
}
body {
  font-family: "Lobster", "Comic Sans", cursive;
}
```

*Before using a font, be sure you have the right to, as per the licensing terms.*

###Citations and Quotes
When to use which appropriate HTML element
* `<cite>` - for a creative work, author or resource.
* `<q>` - for short, inline quotations.
* `<blockquote>` - for longer, external quotations.

