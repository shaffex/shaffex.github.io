# Frame

**Description**

Positions this view within an invisible frame with the specified dimensions.

**Parameters**

- `width`: The width of the frame.
- `height`: The height of the frame.
- `minWidth`: The minimum width of the frame.
- `maxWidth`: The maximum width of the frame.
- `minHeight`: The minimum height of the frame.
- `maxHeight`: The maximum height of the frame.
- `idealWidth`: The ideal width of the frame.
- `idealHeight`: The ideal height of the frame.

**Example**

```xml
<body>
    <list>
        <text width="100" height="100" border="color:red;width:1">100x100</text>
        <text maxWidth="infinity" height="50" border="color:red;width:5">maxWidth=infinity</text>
        <text width="100" height="50" border="color:green;width:2">100x50</text>
        <text width="150" height="100" border="color:blue;width:3">150x100</text>
    </list>
</body>
```
<img src="/Screenshots/Modifiers/Layout/frame_1.png" width="250" alt="Screenshot">
