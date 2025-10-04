# TextField

**Description**

A control that displays an editable text interface.

**Parameters**

- `key`: A binding to a string value that provides the text to display and edit.
- `value`: The initial text to display.
- `axis`: The axis along which the text field can grow. Can be `horizontal` or `vertical`.
- The text content of the tag is used as the placeholder.

**Example**

```xml
<body>
    <form>
        <textfield key="username">Username</textfield>
        <textfield key="multiline" axis="vertical">Enter multiple lines of text...</textfield>
    </form>
</body>
```

<img src="/Screenshots/Views/Controls/textfield_1.png" width="250" alt="Screenshot">
