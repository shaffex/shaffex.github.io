# Image

**Description**

A view that displays an image.

**Parameters**

- `key`: A key to access an image from the environment.
- `systemName`: The name of a system symbol image.
- `variableValue`: A numeric value used for variable symbols.
- `resizable`: A boolean indicating whether the image is resizable.
- `renderingMode`: The rendering mode of the image. Can be `original` or `template`.
- The text content of the tag is the name of the image in the asset catalog.

**Example**

```xml
<body>
    <hstack spacing="20">
        <image systemName="heart.fill" font="largeTitle" foregroundColor="red"/>
        <image resizable="" aspectRatio="fit" frame="width:100">my-logo</image>
    </hstack>
</body>
```
