# AsyncImage

**Description**

A view that asynchronously loads and displays an image.

**Parameters**

- `resizable`: A boolean indicating whether the image is resizable.
- `renderingMode`: The rendering mode of the image. Can be `original` or `template`.
- The text content of the tag is the URL of the image.

***Fit Image Example:***

The example below shows how to load an image from a URL. The `resizable` attribute allows the image to be resized, and `scaledToFit` scales the image to fit its container while maintaining its aspect ratio.

```xml
<body>
    <asyncimage resizable="" scaledToFit="">url:https://magic-ui.com/Demo/Resources/Images/noobie.png</asyncimage>
</body>
```
<img src="/Screenshots/Views/Other/asyncimage_1.png" width="250" alt="Screenshot">

***Fill Image Example:***

This example uses `scaledToFill`, which scales the image to fill its container, potentially cropping the image if its aspect ratio doesn't match.

```xml
<body>
    <asyncimage resizable="" scaledToFill="">url:https://magic-ui.com/Demo/Resources/Images/noobie.png</asyncimage>
</body>
```
<img src="/Screenshots/Views/Other/asyncimage_2.png" width="250" alt="Screenshot">

***Template Image Example:***

This example demonstrates the use of `renderingMode="template"`. This mode allows the image to be colored by the `foregroundColor`. The example also sets a fixed `height` for the image.

```xml
<body>
    <asyncimage resizable="" scaledToFit="" height="200" foregroundColor="red" renderingMode="template">url:https://magic-ui.com/Demo/Resources/Images/noobie.png</asyncimage>
</body>
```
<img src="/Screenshots/Views/Other/asyncimage_3.png" width="250" alt="Screenshot">

***Stretched Image Example:***

When `resizable` is present without any scaling (`scaledToFit` or `scaledToFill`) or size constraints, the image will stretch to fill its parent view.

```xml
<body>
    <asyncimage resizable="">url:https://magic-ui.com/Demo/Resources/Images/noobie.png</asyncimage>
</body>
```
<img src="/Screenshots/Views/Other/asyncimage_4.png" width="250" alt="Screenshot">

***Original Size Example:***

If the `resizable` attribute is not included, the image will be displayed at its original size and will not be resized.

```xml
<body>
    <asyncimage>url:https://magic-ui.com/Demo/Resources/Images/noobie.png</asyncimage>
</body>
```
<img src="/Screenshots/Views/Other/asyncimage_5.png" width="250" alt="Screenshot">
