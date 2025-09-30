# Text

**Description**

A view that displays one or more lines of read-only text.

**Parameters**

- `markdown`: A boolean indicating whether to interpret the text as Markdown. `true` or `false`.
- The content of the tag is the text to display.

**Example**

```xml
<body>
    <vstack alignment="leading" spacing="10">
        <text>This is a plain text.</text>
        <text markdown="true">**This is a bold text in Markdown.**</text>
    </vstack>
</body>
```
