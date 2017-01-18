#Adding Media

##Images
to embed images, simply use the `<img>` tag. It is self containing. Too, be sure to include an `alt` attribute so that the search engines an pick up on it as well as screen readers.

The most commonly supported formats are `gif` `jpg` and `png`.
> `jpg` enables high color count for a low image size. Optimal for pictures. `png` is suited for images with low color count or transparencies.

It's often best to specify only the `width` or `height` for an image. This makes sure to maintain the image's aspect ratio.

###Positioning Images.
By default, images are shown **inline**. But with CSS it is of course possible to switch up the manner in which they are displayed. So, an `img` with no style props will appear incline and force the height of the line in which it appears to match it's own height.

Block positioning images `display: block` ensures that the image appears on its own line and other content surround it. 
> To position an image left or right, one must not only `float`, but also make use of padding and margin properties as are necessary to make other content sit properly around the image.

####When to use `img` element vs `background-image` property
If the image has semantic value on the oage, `img` is the right choice. If however, the image is simply for aesthetic reasons (design or UI of the page), using the `background-image` property is more appropriate.  


##Audio
The `audio` element specifies audio to embed in a web page. Like the `img` tag, it accepts a `src` attribute pointing to the media source.

**Attributes**
* `autoplay` - boolean to make the audio play on load
* `controls`- boolean to make the controls visible
* `preload` - `none, auto, metadata`. determines what, if any information should be loaded before the clip is played. 
* `loop`- boolean to make the audio repeat indefinitely

###Audio fallbacks and multiple sources.


