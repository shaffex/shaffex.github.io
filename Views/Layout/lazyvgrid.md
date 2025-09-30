**LazyVGrid** is a view that arranges its children in a grid with flexible vertical rows. The alignment and spacing parameters determine how the views are aligned and spaced.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the LazyVGrid. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.
> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the rows in the grid.
> **Default value:** System default spacing

`columns` (optional) This parameter determines the grid structure. It's an array of GridItem objects that describe the layout of the grid's columns.

`gridItems` (optional) This parameter determines the grid structure. It's an array of GridItem objects that describe the layout of the grid's columns.
* `adaptive` text `minimum` `maximum` `spacing` `alignment`
* `flexible` text
* `fixed` text


> **Note:** You need to specify columns or gridItems

