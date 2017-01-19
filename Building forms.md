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
Besides the already mentioned uses of the `input` tag, it is also possible to use it in other contexts
