# Modifier Plugins

To create your custom modifier plugin

```swift
import SwiftUI
import MagicUiFramework

struct SxModifier_flipX: SxCustomModifierProtocol {
    @EnvironmentObject var sxEnv: SxEnvironmentObject
    var parameter: String = ""
    var view: SxNodeView?
    
    func body(content: Content) -> some View {
        content.scaleEffect(x: -1, y: 1, anchor: .center)
    }
        
    static func getModifier<Content: View>(content: Content, parameter: String, view: SxNodeView?) -> AnyView {
        AnyView(content.modifier(SxModifier_flipX(parameter: parameter, view: view)))
    }
}
```

Install plugin:
```swift
SxMagicUiView.installModifierPlugin(name: "flipX", plugin: SxModifier_flipX.self)
```

```swift
struct SxModifier_rotateDegrees: SxCustomModifierProtocol {
    @EnvironmentObject var sxEnv: SxEnvironmentObject
    var parameter: String = ""
    var view: SxNodeView?
    
    func body(content: Content) -> some View {
        content
            .rotationEffect(.degrees(parameter.convertToDouble() ?? 0.0), anchor: .center)
    }
        
    static func getModifier<Content: View>(content: Content, parameter: String, view: SxNodeView?) -> AnyView {
        AnyView(content.modifier(SxModifier_rotateDegrees(parameter: parameter, view: view)))
    }
}
```

Install your modifier by calling:

```swift
SxMagicUiView.installModifierPlugin(name: "rotateDegrees", plugin: SxModifier_rotateDegrees.self)
```

When modifier is installed you can apply it anywhere by calling it's attribute in xml:

```xml
<body>
  <vstack rotateDegrees="45">
    <text font="largeTitle">Hello MagicUI</text>
  </vstack>
</body>
```
