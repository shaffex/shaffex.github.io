# Shape: RoundedRectangle

**Description**

A rectangle shape with rounded corners, aligned inside the frame of the view containing it.

**Parameters**

- `cornerRadius`: The corner radius of the rounded rectangle.
- `stroke`: A dictionary specifying the stroke parameters, e.g., `lineWidth`, `dash`.

**Example**

```xml
<body>
    <vstack padding="">
        <roundedrectangle cornerRadius="25" foregroundColor="indigo"/>
        <roundedrectangle cornerRadius="64" stroke="lineWidth:2" foregroundColor="teal" padding="20"/>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Other/roundedrectangle_1.png" width="250" alt="Screenshot">
