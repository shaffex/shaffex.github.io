# Shape: Circle

**Description**

A circle shape aligned inside the frame of the view containing it.

**Parameters**

- `stroke`: A dictionary specifying the stroke parameters, e.g., `lineWidth`, `dash`.

**Example**

```xml
<body>
    <vstack padding="">
        <circle foregroundColor="green"/>
        <zstack>
            <circle foregroundStyle="style:lineargradient;colors:[red,blue];startPoint:0.0,0.5;endPoint:1.0,0.5"/>
            <circle stroke="lineWidth:10; dash:5" foregroundColor="yellow"/>
        </zstack>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Other/circle_1.png" width="250" alt="Screenshot">
