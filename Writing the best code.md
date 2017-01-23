#Best Practices for HTML & CSS Coding

##HTML Coding Pratices
The goal is to write well structrued and standards-compliant code. This is becasue poor code is unreliable, as it's behavior cannot be assured to be consistent in different environments. Hence it is best to avoid churning out poorly written code.

> HTML has over 100 elements available for use. So, it's quite a challenge to decide or determine which element is semantically appropriate for certain content.
If you're uncertain of the choice of element(s) you have made, have a friend review your code for you.

Always use the proper document structure, by which it is meant - `doctype`, `html`, `head` and `body` tags.

In keeping the syntax organized, it's helpful to:
* Indent nested elements.
* Strictly use double quotes while avoiding missing or single quotes.
* Remove the forward slash at the end of self-closing elements.
* Omit the values on boolean attributes. 

When creating ID and class values, be practical. The values should be related to the meaning of the content not the stylign to eb applied to it.

Use alternative text attribute - `alt` on `img` elements. If an image doesn't have a meaningful value, it's best included as a CSS background image 
rather than with an `img` element.

**NEVER** style content within HTML. Rather, be sure to define styles in an external sheet and then reference from your markup. 

It's usually wise to review old code from time to time in order to make it better, condense it or otherwise just improve it.

##CSS Coding Pratices

Organize code with comments. i.e. use comments to separate the styles into sections so they are readabel and searchable.

Write CSS code using multiplie lines and spaces. Also be sure to indent property declarations within selectors.

Class names should be all be lower case and use hyphen-delimiters.

Build efficient selectors - The longer a selector and the number of prequalifiers it requires, the higher its specificity wil be and the more likely it will be to break the cascade and cause undesirable behavior.

Favor classes over very specific selectors.

Be biased towards using shorthand properties and values instead of their long hand alternatives.

Drop units from 0 values.

Group and Align Vendor-prefixes - It makes things much easier or legible to read. Ensure that the property names or values stack vertically. also place unprefexied versions ofthe properties last in the group.


