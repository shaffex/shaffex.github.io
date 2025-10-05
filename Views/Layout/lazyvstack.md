# LazyVStack

**Description**

A view that arranges its children in a vertical line, creating items only as needed.

**Parameters**

- `alignment`: The horizontal alignment of the content in the stack. Can be `leading`, `center`, `trailing`.
- `spacing`: The spacing between items.

**Example**

```xml
<body>
    <scrollview>
        <lazyvstack spacing="10">
            <foreach repeatCount="100">
                <text>Item</text>
            </foreach>
        </lazyvstack>
    </scrollview>
</body>
```
<img src="/Screenshots/Views/Layout/lazyvstack_1.png" width="250" alt="Screenshot">
