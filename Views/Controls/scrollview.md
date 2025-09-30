# ScrollView

**Description**

A scrollable view.

**Parameters**

- `axes`: The scrollable axes. Can be `horizontal` or `vertical` (default).
- `showsIndicators`: A Boolean value that determines whether the scroll view displays scroll indicators.

**Example**

```xml
<body>
    <scrollview>
        <vstack spacing="20">
            <foreach repeatCount="50">
                <text>Item</text>
            </foreach>
        </vstack>
    </scrollview>
</body>
```
