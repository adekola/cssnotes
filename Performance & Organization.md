#Optimization and Performance

Having a solid grasp of HTML and CSS is just one part of the puzzle. A key skill is being able to optmiize the perfromance and speed of the websites too.
The organizationand architecture of a code base can affect both the speed of development as well as the speed at which pages render. To this end, it is relevant to take the time to identify how
all the different components will work together.

##Strategy & Structure
The first step revolves around identifying a good strategy and structure for developing the code base, i.e. building a strong dir structure, outlining design patterns 
as well as finding ways to re-use common code.

###Style Architecture
One practice includes sperarting styles based on intent into directories e.g. for common base styles (variable and typography) , UI components (specific UI elements) and then business logic (for certain sections in pages) for instance.
> If you start to think of websites in terms of systems and not just pages, you will come to appreciate the need for a code architecture which supports sucha mindset.

####Object-Oriented CSS
Proposed by Nicle Sullivan , this approach hinges on 2 principles:
* Separate structure from skin - abstract the layout of an element form the theme of the website.
* Separate content from container -  remove the dependency of a parent element nesting children elements.

In all, OOCSS advocates building a component library, staying flexible and utilizing a grid.

####Scalabe and Modular Architecture for CSS
Developed and advocated by Jonathan Snook, this approach promotes breaking up styles into 5 main categories:

* Base - core elements, coevrign the general defaults.
* Layout - identfies the sizing and grid styles of different elements, determinig their layout.
* Module - specific styles targeting individual parts of th epage e.g. navigation or features.
* State - intended to augment other styles, in case a modeul has alternate states. 
* Theme - built around skin or the look and feel of different modules.

In choosing which methodology to adopt, it's often best to pick the most suitbale aspects of SMACSS and OOCSS and use as appropriate to the needs of your project.

###Performance Driven Selectors
While selectors are often ignored in writing CSS, they are very very important. As a matter of fact, poorly written selectors affect
performance as well as modular and practical the styles are in the overall architecture.

####Keep Selectors Short
For one, this reduces specificity, making for better inheritance and portability. Selectros which are not so specific are less likely to break if there's a change in the order of elements. It's generally a good idea to give all selectors the same specificity, so they can cooperate better.

####Favor Classes
Keeping in mind that the key selector is the unit furthest to the right, watch out for what you use in this position. Use classes freely as key selectors.
Also, **do not prefix class selectors with an element**. Doing so prevents such styles from being applied to a different element.

###Reusable Code
A quick way to reduce file sizes is to be sure to reuse styles. Any repeating styles or interface patterns should be combined, so that code can be shared.

###Minify & Compress fiiles. 
####gzip Compression
As a popular compression method, it is well supported by Apache servers, only requiring an `.htaccess` file in the root directory which specifies which files should be gzipped.

####Image Compression
It's good practice to compress images as well. Compression can be done for images without loss of quality (programs like [PNGGauntlet](https://pnggauntlet.com/). It only removes unnecssary color profiles as well as comments. Also, make it a practise to set the `width` and `height` property in `img` tag as this imporves load time since the space for the image is already laid out.

####Reduce HTTP Requests
Another common performance pitfall is the number of requests which a page makes. The performance degrades seriously per HTTP request which it has to make. Avoid this by doing a number of things.

**Combine like files**
For instance, combine CSS files into one and not make separate requests for each one. Also think to combine JS scripts into a single one.

**Image Sprites**
This involves using one backgroundimage across several elements, thus cutting down on the numbe rof request that have to be made. The trick here is to use the `background-position` property to properly determine which part of the image is displayed. 

**Image Data URI**
Instead of spriting images, the encoded data of an image could be included directly within the HTML and CSS. This of course is ideal for images which rarely change and can be cached effectively. 

####Cache common files
In the `.htaccess` file for Apache serves, the cahceexpiration limit for files can be set. Better still, you can use the one from [HTML Boilerplate](https://github.com/h5bp/server-configs-apache/blob/master/src/web_performance/expires_headers.conf)
