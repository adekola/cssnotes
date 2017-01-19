#Building Forms

##HTML Elements for marking up a form

* `form` - supports the attributes `action` and `method`, among others.
*  `input` - supports the attributes `type` and  `name` among others. It's self containd and doesn't wrap any other element. HTML5 came along with a few new types of `input`
  * `color`
  * `email`
  * `range`
  * `time`
  * `date`
  * `month`
  * `search`
  * `url`
  * `datetime`
  * `number`
  * `tel`
  * `week`
  
*  `textarea` - supports the input of larger text spanning multiple lines. attributes like `cols` and `rows` determine the size of input which is diplayed by the control.

###Multiple choice controls

**Radio Buttons**

These are `input` elements with `type` set to radio. Ensure all related options have the same `name` attribute. 

**Checkboxes**

These are `input` elements with `type` set to checkbox. Ensure all related options have the same `name` attribute. 

**Drop Down Lists**

These are created by the combination of `select` and `option` elements. with the latter neseted witihin the former.


###Form Buttons

* `input` with `type` set to submit. Self-contained just like a regular `input`
* `button` element with `type` set to submit. Has the advanatage that it can enclose other elements.

###Other Inputs
Besides the already mentioned uses of the `input` tag, it is also possible to use it in other contexts. 
* an `input` of type `hidden` allows one to pass data from a form which shouldn't be visible to users.
* an `input` of type `file` allows users to add a file to a form.

###Organizing Form Elements

**Labels**
* `label` to describe the inputs or controls they relate to by using the `for` attribute. It is also possible to wrap target content with the `label` element.

**Fieldsets**
* `fieldset`s, much like `section` wrap related content together within a form for better organization. They include a border outline which may be styled using CSS. 

**Legends**
* `legend`s provide the caption or heading for the `fieldset` element. The `legend` element should be the first child element within a `fieldset` as it wraps the rest of the content within the fieldset.

###Form & Input Attributes

* `disabled` - affects all nested elements if applied to a `fieldset`, also ifapplied to an hidden `input`, makes it ignored.
* `placeholder` - to provide hints of what's expected in an input field.
* `required` - ensures that an element contains a value before it can be submitted to the server. Validation is specific to the type of control e.g. `required` on an email `input` will not only ensure that an input is supplied but that it is also a valid input.
* `accept`
* `formaction`
* `formnovalidate`
* `maxlength`
* `readonly`
* `autocomplete`
* `formenctype`
* `formtarget`
* `min`
* `max`
* `selectionDirection`
* `autofocus`
* `formmethod`
* `pattern`
* `step`




