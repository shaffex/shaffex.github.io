# View Plugins

Magic UI is designed to be easily extensible by developers, allowing the creation of custom views that seamlessly integrate with your application. There are two primary methods for creating custom views, each suited for different needs and complexity levels.

## Option 1: View with MagicNode and Custom Attributes

This approach lets you create a custom view that can access and utilize attributes defined in XML, providing greater control over the view's customization and behavior.

### Example: Text with Subtitle
This example demonstrates creating a simple view that displays a title and subtitle, both definable in XML.
The custom view plugin must conform to the `CustomViewPlugin` protocol.

```swift
struct TextWithSubtitle: SxViewProtocol {
    @DynamicNode var node: MagicNode
    
    var body: some View {
        VStack(alignment: .leading) {
            Text(node.getAttribute("title") ?? "")
                .font(.title).foregroundStyle(.red)
            Text(node.getAttribute("subtitle") ?? "")
                .foregroundStyle(.secondary)
        }
    }
}
```

### Installation
To make your custom view available in your Magic UI setup:

```swift
MagicUiView.installViewPlugin(name: "textwithsubtitle", plugin: TextWithSubtitle.self)
```

### Usage
You can now use your custom view in XML:
```xml
<textwithsubtitle title="Hello" subtitle="MagicUI"/>
```

## Option 2: View with MagicNode, custom attributes and @State variables

Use this when your view needs local mutable state (e.g., counters, toggles) managed by SwiftUI.
Because the view uses @State and @DynamicNode, you must provide a custom initializer that accepts a MagicNode.

### Why an initializer is required
- `@DynamicNode` needs the incoming `MagicNode` bound to your view instance.  
- When a view contains property wrappers like `@State`, Swift will **not** synthesize the memberwise initializer you might expect.  
- Magic-UI’s plugin loader constructs your view by passing the node → therefore your view needs `init(node: MagicNode)`.  

### Example: Counter with local state

```swift
struct CounterView: SxViewProtocol {
    @DynamicNode var node: MagicNode
    
    @State var counter = 0
    
    // If you using @State variables, you need to create custom initializer
    init(node: MagicNode) {
        self.node = node
    }
    
    var body: some View {
        VStack() {
            Text(node.getAttribute("title") ?? "")
                .font(.title).foregroundStyle(.red)
            Text("\(counter)")
                .foregroundStyle(.secondary)
            HStack {
                Button("⊕") {
                    counter += 1
                }
                Button("⊖") {
                    counter -= 1
                }
            }
            .font(.title)
        }
        .background(.yellow.opacity(0.3))
    }
}
```

### Installation
To make your custom view available in your Magic UI setup:

```swift
MagicUiView.installViewPlugin(name: "counterview", plugin: CounterView.self)
```

### Usage
You can now use your custom view in XML:
```xml
<counterview title="Counter"/>
```

## Option 3: Using SwiftUI Views

This option allows you to integrate existing SwiftUI views or create new ones without handling custom attributes, making it perfect for simpler use cases or when working with existing SwiftUI components.

### Example: Clock View
Here's an example of a clock view that updates every second:
```swift
struct ClockView: View {
    @State private var currentTime = Date()
    @State private var ticks = 0
    
    private var timer = Timer.publish(every: 0.01, on: .main, in: .common).autoconnect()
    
    var body: some View {
        VStack(alignment: .leading) {
            Text(currentTime, style: .time)
                .font(.largeTitle)
                .onReceive(timer) { input in
                    self.currentTime = input
                    self.ticks += 1
                }
            Text("Ticks: \(ticks)").monospacedDigit()
        }
        .onAppear {
            self.currentTime = Date()
        }
    }
}
```

### Installation
Register the view for use in your XML layouts:
```swift
MagicUiView.installViewPlugin(name: "clockview", plugin: ClockView())
```

### Usage
Use the clock view in your XML:
```xml
<clockview/>
```
