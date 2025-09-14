# Background Material

**Description**

Applies a background material to the view, creating a translucent, blurred effect that adapts to the content behind it.

**Parameters**

- `material`: The type of material to apply.
  - `regular`: The default material.
  - `ultrathin`: A very thin and translucent material.
  - `thin`: A thin, translucent material.
  - `thick`: A thick, less translucent material.
  - `ultrathick`: A very thick and opaque material.
  - `bar`: A material suitable for bars and other chrome elements.

**Examples**

```xml
<body>
<zstack>
    <image systemImage="photo" resizable="" aspectRatio="fill" ignoresSafeArea=""/>
    <vstack spacing="10" padding="20" foregroundColor="primary">
        <text font="headline" fontWeight="bold">Background Materials</text>
        <text backgroundMaterial="regular" padding="10" cornerRadius="8">Regular</text>
        <text backgroundMaterial="thin" padding="10" cornerRadius="8">Thin</text>
        <text backgroundMaterial="ultrathin" padding="10" cornerRadius="8">Ultra Thin</text>
        <text backgroundMaterial="thick" padding="10" cornerRadius="8">Thick</text>
        <text backgroundMaterial="ultrathick" padding="10" cornerRadius="8">Ultra Thick</text>
        <text backgroundMaterial="bar" padding="10" cornerRadius="8">Bar</text>
    </vstack>
</zstack>
</body>
```
