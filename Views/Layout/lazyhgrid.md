# LazyHGrid

**Description**

A grid that grows horizontally, creating items only as needed.

**Parameters**

- `rows`: The number of rows in the grid.
- `gridItems`: An array of `GridItem` strings that describe the layout of the grid's rows.
- `alignment`: The vertical alignment of the content in the grid. Can be `top`, `center`, `bottom`, `firstTextBaseline`, `lastTextBaseline`.
- `spacing`: The spacing between rows.

**Example**

```xml
<body>
    <scrollview axes="horizontal">
        <lazyhgrid rows="3" spacing="10">
            <foreach repeatCount="30">
                <text padding="10" background="blue" foregroundColor="white">Item</text>
            </foreach>
        </lazyhgrid>
    </scrollview>
</body>
```

<img src="/Screenshots/Views/Layout/lazyhgrid_1.png" width="250" alt="Screenshot">
