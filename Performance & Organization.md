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
* Theme - built around skin or the look and feel of diffeent modules.




