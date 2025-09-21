# Modifier Plugins

## Introduction

The MagicUI framework enables developers to create custom view modifiers that can be reused across their views through modifier plugins. This guide demonstrates how to create, install, and use these custom modifier plugins.

## Creating a Custom Modifier Plugin

To create a custom modifier plugin, implement the `SxModifierProtocol` protocol.

### Example 1: `flipX` Modifier Plugin
This plugin horizontally flips a view's content.

```swift
struct Modifier_flipX: SxModifierProtocol {
    @DynamicNode var node: MagicNode
    
    func body(content: Content) -> some View {
        content.scaleEffect(x: -1, y: 1, anchor: .center)
    }
}
```

To install the plugin:
```swift
MagicUiView.installModifierPlugin(name: "flipX", plugin: Modifier_flipX.self)
```

### Using the Modifier Plugin

After installation, apply the modifier to any view in your XML layout using its attribute:

```xml
<body>
  <vstack flipX="">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```

### Example 2: `rotateDegrees` Modifier Plugin

This plugin rotates a view by a specified number of degrees.

```swift
struct Modifier_rotateDegrees: SxModifierProtocol {
    @DynamicNode var node: MagicNode
    
    func body(content: Content) -> some View {
        content
            .rotationEffect(.degrees(node.convertToDouble() ?? 0.0), anchor: .center)
    }
}
```

To install the plugin:
```swift
MagicUiView.installModifierPlugin(name: "rotateDegrees", plugin: Modifier_rotateDegrees.self)
```

### Using the Rotation Modifier

Apply the rotation modifier to views in your XML layout:

```xml
<body>
  <vstack rotateDegrees="45">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```

## Summary

MagicUI's modifier plugin system provides a straightforward way to create reusable view modifiers. These modifiers can enhance both the functionality and appearance of your SwiftUI views. By implementing them as XML attributes, you gain a flexible and maintainable approach to UI transformations.
