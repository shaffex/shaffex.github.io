**VStack** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.

> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the views.
> **Default value:** System default spacing

## Examples



```xml
<body>
    <vstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Layout/vstack_1.png" width="250" alt="Screenshot">





---
*With no spacing*

```xml
<body>
    <vstack spacing="0">
        <rectangle foregroundColor="red"/>
        <rectangle foregroundColor="green"/>
        <rectangle foregroundColor="blue"/>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Layout/vstack_2.png" width="250" alt="Screenshot">





---
*Combined with hstack*

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
<img src="/Screenshots/Views/Layout/vstack_3.png" width="250" alt="Screenshot">





---
*Combined with hstack*

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
<img src="/Screenshots/Views/Layout/vstack_4.png" width="250" alt="Screenshot">





---
