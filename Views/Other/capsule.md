# Shape: Capsule

**Description**

A capsule shape aligned inside the frame of the view containing it.

**Parameters**

- `stroke`: A dictionary specifying the stroke parameters, e.g., `lineWidth`, `dash`.

**Example**

```xml
<body>
    <vstack padding="">
        <capsule foregroundColor="blue"/>
        <capsule foregroundColor="red"/>
        <zstack>
            <capsule foregroundStyle="style:lineargradient;colors:[red,blue];startPoint:0.0,0.5;endPoint:1.0,0.5"/>
            <capsule stroke="lineWidth:10; dash:5" foregroundColor="yellow"/>
        </zstack>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Other/capsule_1.png" width="250" alt="Screenshot">
