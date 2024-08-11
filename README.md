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

## Plugins

* [Views](./Views.md)
* [Modifiers](./Modifiers.md)
* [Actions](./Actions.md)

## Create your own views
[How to create view plugin](./PluginViews.md)

## Create your own modifiers
[How to create modifier plugin](./PluginModifiers.md)

## Create your own actions
[How to create action plugin](./PluginActions.md)
