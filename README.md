# MagicUI

* [Test](./Test.md)

Welcome to **MagicUI**, a revolutionary user interface framework designed with performance and flexibility in mind. 

## Ultra Lightweight

MagicUI is incredibly lightweight. We've stripped it down to the essentials, making it a perfect choice for projects where every kilobyte counts.

## Blazing Fast Performance

Speed is at the heart of MagicUI. It's optimized for high performance, ensuring your user interfaces are smooth and responsive, even under heavy load.

## Plugin-Based Architecture

MagicUI is built on a plugin-based architecture. This means you can extend and customize it to suit your needs, adding only the features you need and keeping your project lean and efficient.

Experience the magic of user interface development with MagicUI!

## Customised and Blazing Fast XML Parser
Our XML parser is a high-performance, customised solution designed to handle a wide range of XML documents. It's engineered to be blazing fast, making it ideal for applications that require real-time processing of large XML files.
<details>
<summary>Details (Click to expand)</summary>

<h2>Features</h2>

<h3>Support for Comments</h3>

Our parser fully supports XML comments. This means you can include notes in your XML documents without affecting the data that the parser extracts.

```xml
<body>
<!-- This is a comment which will be ignored by parser -->
</text>Hello MagicUI!</text>
</body>
```

<h3>CDATA Support</h3>

```xml
<body>
<text><![CDATA[Any special characters like <>&']]></text>
</body>
```

The parser also supports CDATA sections, allowing you to include text that the parser will not interpret as XML markup. This is useful for including content such as scripts or HTML markup in your XML documents.

<h3>Ordered Attributes</h3>

Unlike many XML parsers, our solution maintains the order of attributes in XML elements. This can be crucial for applications where the order of attributes matters like in SwiftUI views.

```xml
<body>
<text font="largeTitle" background="yellow" padding="20">MAGIC UI</text>
</body>
```

```xml
<body>
<text font="largeTitle" padding="" background="yellow">MAGIC UI</text>
</body>
```
</details>

# How to integrate Magic UI into your project

### Step 1: Add Swift Package and import Magic UI framework

To start using Magic UI in your Swift project, the first step is to add Swift Package and import the MagicUiFramework. This framework provides all the necessary classes and methods to create and render dynamic UI components based on XML.


#### Add this Swift Package:
```
https://gitlab.com/magicui/magicui-framework-beta.git (will be updated)
```
#### Import 'MagicUiFramework' into your SwiftUI file:
```swift
import MagicUiFramework
```

### Step 2: Choose Your Data Source

Magic UI allows you to create views from various sources depending on where your XML data is stored. You can load the UI from a string, a local resource, a file, or a URL. Choose the method that best suits your use case.

#### Option 1: Initialize with a String
If your XML data is stored as a string, you can directly pass it to MagicUiView.

```swift
MagicUiView(string: "<body><text>Welcome to Magic UI!</text></body>")
```

#### Option 2: Initialize with a Resource
If your XML data is embedded within your app's resources (e.g., within your Xcode project), you can reference it by name. The framework will look for the corresponding XML file in your bundle.

```swift
MagicUiView(resource: "MainScreen")
```

#### Option 3: Initialize with a File Path
You can also load an XML file from a specific path within the app's file system. The root is app's Documents folder

```swift
MagicUiView(file: "MYView.xml")
```

#### Option 4: Initialize with a URL
If your XML content is hosted remotely, you can load it directly from a URL. Magic UI will handle fetching and rendering the content.

```swift
MagicUiView(url: "https://example.com/myView.xml")
```

#### Step 3: There is No Step 3! It's That Simple.
Once you've chosen and implemented your data source, Magic UI takes care of rendering the view for you. No additional steps are required. Your UI is now ready to be displayed with minimal setup.

#### Full Example: Rendering MagicUiView from a String
Here's a complete example of how to render a Magic UI view from an XML string within a SwiftUI application:

```swift
import SwiftUI
import MagicUiFramework


struct ContentView: View {
    var body: some View {
        MagicUiView(string: "<body><text>Hello Magic UI!</text></body>")
    }
}

#Preview {
    ContentView()
}
```

## Available Plugins

### Views
* [Supported Views](./Views.md)
* [How to create view plugin](./PluginViews.md)

### Modifiers
* [Supported Modifiers](./Modifiers.md)
* [How to create modifier plugin](./PluginModifiers.md)

### Actions
* [Supported Action](./Actions.md)
* [How to create action plugin](./PluginActions.md)
