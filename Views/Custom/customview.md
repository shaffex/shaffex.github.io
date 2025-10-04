# CustomView

**Description**

A view that displays a reusable view defined elsewhere in the XML.

**Parameters**

- `src`: The `id` of the view to render.

**Example**

```xml
<body>
    <customview src="myReusableView"/>
    <vstack id="myReusableView">
        <text>This is a reusable view.</text>
    </vstack>
</body>
```

<img src="/Screenshots/Views/Custom/customview_1.png" width="250" alt="Screenshot">
