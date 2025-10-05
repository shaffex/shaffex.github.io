**HStack** is a view that arranges its children in a horizontal line. The alignment parameter determines how the views are aligned vertically.

***Parameters:***

`alignment` (optional) This parameter determines the vertical alignment of the views within the HStack. It's of type VerticalAlignment and can take the following values:
* `top` Aligns the views along the top edge.
* `center` Aligns the views along the center.
* `bottom` Aligns the views along the bottom edge.
* `firstTextBaseline` Aligns the first line of text in each view along a common baseline.
* `lastTextBaseline` Aligns the last line of text in each view along a common baseline.

> **Default value:** center

`spacing` (optional) This parameter determines the horizontal spacing between the views.
> **Default value:** System default spacing

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
<img src="/Screenshots/Views/Layout/hstack_1.png" width="250" alt="Screenshot">




---


```xml
<body>
    <hstack spacing="0">
        <rectangle foregroundColor="red"/>
        <rectangle foregroundColor="green"/>
        <rectangle foregroundColor="blue"/>
    </hstack>
</body>
```
<img src="/Screenshots/Views/Layout/hstack_2.png" width="250" alt="Screenshot">




---
*Example with various spacings*

```xml
<body>
    <vstack>
        <text>spacing 0:</text>
        <hstack spacing="0">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
        <text>spacing 20:</text>
        <hstack spacing="20">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
        <text>spacing 100:</text>
        <hstack spacing="100">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Layout/hstack_3.png" width="250" alt="Screenshot">




---
*Example with various alignments*

```xml
<body>
    <vstack>
        <text>top alignment:</text>
        <hstack alignment="top">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
        <text>center alignment:</text>
        <hstack alignment="center">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
        <text>bottom alignment:</text>
        <hstack alignment="bottom">
            <rectangle foregroundColor="red"/>
            <circle foregroundColor="green"/>
            <rectangle foregroundColor="blue"/>
        </hstack>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Layout/hstack_4.png" width="250" alt="Screenshot">




---
