# Shape: Rectangle

**Description**

A rectangle shape aligned inside the frame of the view containing it.

**Parameters**

- `stroke`: A dictionary specifying the stroke parameters, e.g., `lineWidth`, `dash`.

**Example**

```xml
<body>
    <vstack padding="">
        <rectangle foregroundColor="cyan"/>
        <rectangle stroke="lineWidth:5;dash:5" foregroundColor="mint" clipped=""/>
        <rectangle foregroundStyle="style:lineargradient;colors:[red,blue];startPoint:0.0,0.5;endPoint:1.0,0.5"/>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Other/rectangle_1.png" width="250" alt="Screenshot">
