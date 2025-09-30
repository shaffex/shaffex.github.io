# PhotosPicker

**Description**

A view that allows the user to pick photos and videos from their photo library.

**Parameters**

- `title`: The title of the picker.
- `matching`: The type of assets to filter for. Can be `images`, `videos`, `livePhotos`, etc.
- `key`: The key to store the selected asset.

**Example**

```xml
<body>
    <photospicker title="Select an Image" matching="images" key="selectedImage"/>
    <image if="$selectedImage != nil" key="selectedImage" resizable="" aspectRatio="fit" frame="height:200"/>
</body>
```
