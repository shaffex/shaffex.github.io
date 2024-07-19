## Controls
<details markdown="block">
<summary>button</summary>

### 

***Button12345*** is a container that stacks its children vertically.

`iOS 13+` `MacOSX` `Tag3`

</details>
<details markdown="block">
<summary>datepicker</summary>
    
datepicker is a container that stacks its children vertically.
</details>
<details markdown="block">
<summary>link</summary><br>
link is a container that stacks its children vertically.

</details>
<details markdown="block">
<summary>list</summary><br>
list is a container that stacks its children vertically.


</details>

## Layout
<details markdown="block">
<summary>vstack</summary><br>
**VStackKOKOCE** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

> **Note:** Piknova

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.



> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the views.
> **Default value:** System default spacing

## Examples

*Example 1: How to pickup a Noob*

```xml
<body>
    <foreach repeatCount="8">
    <hstack>
        <rectangle foregroundColor="red"/>
        <rectangle foregroundColor="orange"/>
        <rectangle foregroundColor="red"/>
    </hstack>
    </foreach>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-0.png" alt="KOKOCE ALT" width="250"/>

---


```xml
<body>
    <vstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>
    </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-1.png" alt="KOKOCE ALT" width="250"/>

---


```xml
<body>
  <vstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-2.png" alt="KOKOCE ALT" width="250"/>

---
*Toto je priklad 4*

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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-3.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>hstack</summary><br>
HStack is a container that stacks its children vertically.

## Examples

*Hstack example*

```xml
<body>
    <hstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>        
    </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-0.png" alt="KOKOCE ALT" width="250"/>

---


```xml
<body>
  <hstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-1.png" alt="KOKOCE ALT" width="250"/>

---


```xml
<body>
  <vstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-2.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>zstack</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>lazyvgrid</summary><br>
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


</details>
<details markdown="block">
<summary>geometryreader</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>viewthatfits</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>

## Paint
<details markdown="block">
<summary>lineargradient</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>radialgradient</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>

## Others

## Custom
<details markdown="block">
<summary>scrollingtext</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>webview</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>videoview</summary><br>
ZStack is a container that overlays its children, aligning them in both axes.


</details>
