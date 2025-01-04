# Modifier Plugins

## Introduction

Modifier plugins in the MagicUI framework allow developers to create custom view modifiers that can be reused across their views. This guide will walk you through the steps to create, install, and use custom modifier plugins.

## Creating a Custom Modifier Plugin

To create a custom modifier plugin, you need to conform to the `CustomModifierPlugin` protocol.

### Example 1: `flipX` Modifier Plugin
The flipX plugin horizontally flips the content.

```swift
struct SxModifier_flipX: SxModifierProtocol {
    @DynamicNode var node: MagicNode
    
    func body(content: Content) -> some View {
        content.scaleEffect(x: -1, y: 1, anchor: .center)
    }
}
```

Install plugin:
```swift
MagicUiView.installModifierPlugin(name: "flipX", plugin: Modifier_flipX.self)
```

####Using the Modifier Plugin in XML:

Once a modifier plugin is installed, you can apply it to any view within your XML layout by using its corresponding attribute:

```xml
<body>
  <vstack flipX="">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```

### Example 2: `rotateDegrees` Modifier Plugin

```swift
struct SxModifier_rotateDegrees: SxModifierProtocol {
    @DynamicNode var node: MagicNode
    
    func body(content: Content) -> some View {
        content
            .rotationEffect(.degrees(node.convertToDouble() ?? 0.0), anchor: .center)
    }
}
```

Install your modifier by calling:

```swift
MagicUiView.installModifierPlugin(name: "rotateDegrees", plugin: Modifier_rotateDegrees.self)
```

#### Using the Modifier Plugin in XML:

Once a modifier plugin is installed, you can apply it to any view within your XML layout by using its corresponding attribute:

```xml
<body>
  <vstack rotateDegrees="45">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```

## Summary

Creating and installing custom modifier plugins in MagicUI is straightforward. By following the steps outlined above, you can build reusable view modifiers that enhance the functionality and appearance of your SwiftUI views. Once installed, these modifiers can be easily applied to views through XML attributes, providing a flexible and powerful way to manage UI transformations.
