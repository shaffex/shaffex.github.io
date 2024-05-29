**VStack** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.



> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the views.
> **Default value:** System default spacing
<details markdown="block">
<summary>Click me now</summary>

 <div id="code">

```xml
<body>
    <foreach repeatCount="8">
    <hstack>
        <rectangle foregroundColor="red"/>
        <rectangle foregroundColor="orange"/>
        <rectangle foregroundColor="red"/>
    </hstack>
    </foreach>
<script src="https://cdnjs.cloudflare.com/ajax/libs/clipboard.js/2.0.8/clipboard.min.js"></script>
</body>



```
</div>
    <button class="btn" data-clipboard-target="#code">Copy Code</button>

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://shaffex.com/MagicUiDemo/Help/images/noob2.png)

<details markdown="block">
<summary>Click me now</summary>

```xml
<body>
    <foreach repeatCount="8">
    <hstack>
        <rectangle foregroundColor="blue"/>
        <rectangle foregroundColor="orange"/>
        <rectangle foregroundColor="red"/>
    </hstack>
    </foreach>
</body>
```
![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://shaffex.com/MagicUiDemo/Help/images/noob2.png)

 <script src="https://cdnjs.cloudflare.com/ajax/libs/clipboard.js/2.0.8/clipboard.min.js"></script>

</details>

</details>

<details markdown="block">

```xml
<body>
    <vstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>
    </vstack>
</body>
```
</details>

<details markdown="block">

```xml
<body>
  <vstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </vstack>
</body>
```
</details>

<details markdown="block">

```xml
<body>
  <hstack>
      <rectangle foregroundColor="yellow"/>
      <vstack>
          <rectangle foregroundColor="red"/>
          <rectangle foregroundColor="green"/>
          <rectangle foregroundColor="blue"/>
      </vstack>
      <rectangle foregroundColor="yellow"/>
  </hstack>
</body>
```
</details>


---

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
