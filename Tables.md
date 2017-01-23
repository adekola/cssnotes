#Tables

##Creating a table
* `table` - the main enclosing element defining the table.
* `tr` - defines a row in the table.
* `td` - defines a cell within a `row` in a table.
* `th` - defines a cell header for a table. Attribute `scope` with values `col, row, colgroup or rowgroup` determine the semantic value of the content which the table header relates to.

> Should there be a need to relate a cell `td` or `th` to a different header, the `headers` attribute of the `th` can be set to match the id of the target `th`.

###Table Structure
**Caption**
The `caption` element describes what the table contains. Must come immeditalye after the opening table tag.

* `thead` - wraps the heading row or rows.
* `tbody` - wraps the primary data in the table.
* `tfoot` - summary data for the table.

> `colspan` and `rowspan` attributes on `td` or `th` elements specify the no of cols and rows respectively which the cell should span.

###Table Borders
`border-collapse` property allows one to determine the border model for a table, given that nested cells will have their own border specs indepenedent of the table and this couldcause duplicate borders in several cases.
Values include `collapse, **separate**, inherit`.

`border-spacing` determines how much space if any would be set between the borders. This property onley works when the `border-collapse` property is set to `separate`, it's default value. In addition, this property can accept 2 values - one for the horizontal spacing and the other for the vertical spacing (respectively).

###Aligning Text
String values are often flush left while numbers are often flush right. `vertical-align: {top, middle, bottom}` and `text-align` properties help to achieve this. Note that `vertical-align` only applies to inline elements and tabel cells. It won't work for block, inline-block or other element levels. 

