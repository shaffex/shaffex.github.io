# View

**Description**

A view that loads its content from another view defined in the same XML.

**Parameters**

- `src`: The `id` of the view to render.
- `viewId`: An optional ID for the view.

**Example**

```xml
<body>
    <view src="reusableView"/>
    <text id="reusableView">This is a reusable view.</text>
</body>
```

<img src="/Screenshots/Views/Custom/view_1.png" width="250" alt="Screenshot">
