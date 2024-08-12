# View Plugins

Magic UI is designed to be easily extendable by developers, enabling the creation of custom views that can seamlessly integrate with your application. To create your custom view, you have two primary options, each suited to different needs and levels of complexity.

## Option 1: View with Node Object and Custom Attributes

This method allows you to create a custom view that can access and use attributes defined in XML. It provides more control over the customization and behavior of the view.

### Example: Text with Subtitle
In this example, we create a simple view that displays a title and subtitle, both of which can be defined in the XML.
To create a custom view plugin, you need to conform to the `CustomViewPlugin` protocol.

```swift
struct TextWithSubtitle: CustomViewPlugin {
    let view: SxNodeView?
    
    var body: some View {
        VStack {
            Text(view?.getAttribute("title") ?? "")
                .font(.title)
            Text(view?.getAttribute("subtitle") ?? "")
                .foregroundStyle(.secondary)
        }
    }
    
    static func build(view: SxNodeView?) -> AnyView {
        AnyView(TextWithSubtitle(view: view))
    }
}
```
### Installation
To make this custom view available within your Magic UI setup, install it as follows:

```swift
MagicUiView.installViewPlugin(name: "textwithsubtitle", plugin: TextWithSubtitle.self)
```

### Usage
You can now use your custom view directly in XML:
```xml
<textwithsubtitle title="Hello" subtitle="MagicUI"/>
```


## Option 2: Use Any SwiftUI View

If you already have a SwiftUI view or prefer to create your view using pure SwiftUI without handling custom attributes, this option allows you to easily integrate it with Magic UI.

### Example: Clock View
Here’s a simple example of a clock view that updates every second:
```swift
struct ClockView: View {
    @State private var currentTime = Date()
    
    private var timer = Timer.publish(every: 1, on: .main, in: .common).autoconnect()
    
    var body: some View {
        Text(currentTime, style: .time)
            .font(.largeTitle)
            .onReceive(timer) { input in
                self.currentTime = input
            }
    }
}
```

### Installation
To make this view accessible in your XML layout, install it using the following code:
```swift
MagicUiView.installViewPlugin(name: "clockview", plugin: ClockView())
```

### Usage
You can then use the clock view directly in your XML:
```xml
<clockview/>
```
