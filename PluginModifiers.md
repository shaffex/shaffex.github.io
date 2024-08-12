# Modifier Plugins

To create your custom modifier plugin

```swift
import SwiftUI
import MagicUiFramework

struct Modifier_flipX: CustomModifierPlugin {
    @EnvironmentObject var sxEnv: SxEnvironmentObject
    var parameter: String = ""
    var view: SxNodeView?
    
    func body(content: Content) -> some View {
        content.scaleEffect(x: -1, y: 1, anchor: .center)
    }
        
    static func getModifier<Content: View>(content: Content, parameter: String, view: SxNodeView?) -> AnyView {
        AnyView(content.modifier(Modifier_flipX(parameter: parameter, view: view)))
    }
}
```

Install plugin:
```swift
MagicUiView.installModifierPlugin(name: "flipX", plugin: Modifier_flipX.self)
```

```swift
struct Modifier_rotateDegrees: CustomModifierPlugin {
    @EnvironmentObject var sxEnv: SxEnvironmentObject
    var parameter: String = ""
    var view: SxNodeView?
    
    func body(content: Content) -> some View {
        content
            .rotationEffect(.degrees(parameter.convertToDouble() ?? 0.0), anchor: .center)
    }
        
    static func getModifier<Content: View>(content: Content, parameter: String, view: SxNodeView?) -> AnyView {
        AnyView(content.modifier(Modifier_rotateDegrees(parameter: parameter, view: view)))
    }
}
```

Install your modifier by calling:

```swift
MagicUiView.installModifierPlugin(name: "rotateDegrees", plugin: Modifier_rotateDegrees.self)
```

When modifier is installed you can apply it anywhere by calling it's attribute in xml:

```xml
<body>
  <vstack rotateDegrees="45">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```
