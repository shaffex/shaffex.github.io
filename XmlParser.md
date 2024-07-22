## Xml Parser
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
