# LazyHStack

**Description**

A view that arranges its children in a horizontal line, creating items only as needed.

**Parameters**

- `alignment`: The vertical alignment of the content in the stack. Can be `top`, `center`, `bottom`, `firstTextBaseline`, `lastTextBaseline`.
- `spacing`: The spacing between items.

**Example**

```xml
<body>
    <scrollview axes="horizontal">
        <lazyhstack spacing="10">
            <foreach repeatCount="100">
                <text>Item</text>
            </foreach>
        </lazyhstack>
    </scrollview>
</body>
```

<img src="/Screenshots/Views/Layout/lazyhstack_1.png" width="250" alt="Screenshot">
