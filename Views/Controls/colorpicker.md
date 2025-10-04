# Color Picker

**Description**

A control for selecting a color.

**Parameters**

- `key`: A string representing the key to store the selected color value.
- `value`: The initial color value in hex format (e.g., "#FF0000").
- The text content of the tag is used as the label for the color picker.

**Example**

```xml
<body>
    <form>
        <colorpicker key="selectedColor" value="#FFA500">Choose a color</colorpicker>
        <text>Selected color: $selectedColor</text>
    </form>
</body>
```

<img src="/Screenshots/Views/Controls/colorpicker_1.png" width="250" alt="Screenshot">
