# MagicUI


Note: Help in progress ... if any questions please contact shaffex at support com


Welcome to **MagicUI**, a revolutionary user interface framework designed with performance and flexibility in mind. 

## Platform Support

MagicUI is fully compatible with all Apple platforms:
- iOS
- macOS
- tvOS
- watchOS
- visionOS

This universal compatibility ensures you can use the same framework across your entire Apple ecosystem.

## Key Features

- **Easily Extendable**: Simple plugin architecture to add custom actions, views, and behaviors
- **Intelligent Actions**: Rich set of pre-built actions for common UI interactions and business logic
- **Reactive Variables**: Built-in support for reactive programming with automatic UI updates when data changes
- **File System Integration**: Built-in support for file operations, document handling, and storage management
- **Data Model Support**: Powerful data modeling capabilities with automatic UI binding and persistence
- **Local and Push Notifications**: Seamless integration with local and remote push notifications
- **Multimedia Support**: Easy handling of images, videos, and audio content
- **Local UI Rendering**: Multiple options for UI rendering - from strings, resources, files, and URLs
- **Server-Side Rendering**: Generate and update UI components from your backend
- **Remote UI Updates**: Update your app's interface directly from your server without app updates
- **Smart Caching**: Intelligent caching system for remote content and assets

Experience the magic of user interface development with MagicUI!

## Versatile Usage

MagicUI can be implemented anywhere SwiftUI is supported, making it perfect for:
- Local UI components
- Remote dynamic interfaces
- Widgets and complications
- Live Activities
- App Intents
- App Clips
- Watch complications
- Vision apps

## Ultra Lightweight

MagicUI is incredibly lightweight. We've stripped it down to the essentials, making it a perfect choice for projects where every kilobyte counts.

## Blazing Fast Performance

Speed is at the heart of MagicUI. It's optimized for high performance, ensuring your user interfaces are smooth and responsive, even under heavy load.

## Plugin-Based Architecture

MagicUI is built on a plugin-based architecture. This means you can extend and customize it to suit your needs, adding only the features you need and keeping your project lean and efficient.

Experience the magic of user interface development with MagicUI!

## Customised and Blazing Fast XML Parser
Our XML parser is a high-performance, customised solution designed to handle a wide range of XML documents. It's engineered to be blazing fast, making it ideal for applications that require real-time processing of large XML files.
* [More info about XML Parser](./XmlParser.md)

# How to integrate Magic UI into your project

### Step 1: Add Swift Package and import Magic UI framework

To start using Magic UI in your Swift project, the first step is to add Swift Package and import the `MagicUiFramework`. This framework provides all the necessary classes and methods to create and render dynamic UI components based on XML.


#### Add this Swift Package into your XCode project:
```
https://gitlab.com/magicui/magicui-framework-beta.git (will be updated)
```
#### Import `MagicUiFramework` into your SwiftUI file:
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
> **Note:** Yor resource file must have an extension `xml` so it will be stored in your resources like `MainScreen.xml`

#### Option 3: Initialize with a File Path
You can also load an XML file from a specific path within the app's file system. The root is app's Documents folder

```swift
MagicUiView(file: "MyView.xml")
```

#### Option 4: Initialize with a URL
If your XML content is hosted remotely, you can load it directly from a URL. Magic UI will handle fetching and rendering the content.

```swift
MagicUiView(url: "https://example.com/myView.xml")
```

#### Option 5: Initialize with URL and Caching
If your XML content is hosted remotely, you can load it directly from a URL while enabling offline access. Magic UI will fetch the content and cache it locally for future use, allowing your app to work even without an internet connection.

```swift
// Load from URL with automatic caching
MagicUiView(urlCache: "https://example.com/myView.xml")
```

The cached content will be used when:
- The device is offline
- The remote content is unavailable
- Loading the remote content fails

This ensures your app remains functional regardless of network connectivity.

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
* [Supported Actions](./Actions.md)
* [How to create action plugin](./PluginActions.md)

### Events
* [Supported Events](./Events.md)
* [How to create event plugin](./PluginEvents.md)

### Data Models
* [How to use Data Models](./DataModels.md)
