## Xml Parser

<h2>Features</h2>

<h3>Support for Comments</h3>

Our parser fully supports XML comments. This means you can include notes in your XML documents without affecting the data that the parser extracts.

```xml
<body>
<!-- This is a comment which will be ignored by parser -->
</text>Hello MagicUI!</text>
</body>
```

### CDATA Support
The parser also supports CDATA sections, allowing you to include text that the parser will not interpret as XML markup. This is useful for including content such as scripts or HTML markup in your XML documents.
```xml
<body>
<text><![CDATA[Any special characters like <>&']]></text>
</body>
```

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

### Handling Duplicate Attribute Names in Magic UI XML
When defining UI components in Magic UI using XML, it's important to note that XML specification does not support multiple attributes with the same name within a single element. This can be problematic if you need to apply multiple variations of the same attribute, such as different padding values or multiple background colors.

To address this limitation, Magic UI provides a simple convention: use a postfix with an underscore `_` followed by any string to differentiate attributes that would otherwise have the same name.

Example: Using Postfixes to Differentiate Attributes

Here’s an example of how to define a text element with multiple padding and background attributes:

```xml
<text padding="" background="red" padding_2="" background_2="blue">Hello Magic UI!</text>
```

<details markdown="block">
<summary>xmlparser</summary><br>

This will be help for XML parser

## Examples

*How to use comments*

```xml
<body>
<!-- This is a comment which will be ignored by parser -->
<text>Hello MagicUI!</text>
<!-- This is another comment which will be ignored by parser -->
</body>
```




---
*Commented block will be not rendered*

```xml
<body>
  <!-- This will be not rendered and ignored by parser
  <text>Not rendered</text>
  -->

  <text>Hello MagicUI!</text>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/xmlparser-1.png" alt="KOKOCE ALT" width="250"/>

---
*How to use cdata section to use special characters in xml*

```xml
<body>
  <text padding=""><![CDATA[You can use here any special characters which are not allowed in xml like <>&']]></text>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/xmlparser-2.png" alt="KOKOCE ALT" width="250"/>

---
*XML attributes are processed in order because in SwiftUI, the order of modifiers applied to a view is significant. SwiftUI processes these modifiers in sequence, affecting the final appearance and behavior of the view.*

```xml
<body>
  <vstack>
    <text font="largeTitle" background="yellow" padding="20">MAGIC UI</text>
    <text font="largeTitle" padding="" background="yellow">MAGIC UI</text>
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/xmlparser-3.png" alt="KOKOCE ALT" width="250"/>

---

</details>
