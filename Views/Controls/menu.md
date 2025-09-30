**List** is a container that presents rows of data arranged in a single column, similar to UITableView in UIKit but with a more declarative and simpler syntax. It's commonly used for displaying a collection of items in a structured format and supports features like selection, deletion, and reordering of items if needed.

***Parameters:***

`listStyle` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `automatic` The standard or default list style that automatically adapts to the current platform or theme.
* `plain` A simple, plain style that does not show separators between rows by default and does not indent rows.
* `grouped` This style groups items in sections, similar to the grouped style in UIKit's UITableView. It's often used with a Section view to create distinct groups of items.
* `inset` Provides an inset appearance to the list, with margins on the sides, giving it a card-like feel.
* `insetGrouped` Combines the inset style with grouped sections, offering a modern look with background and spacing around grouped items.
* `sidebar` Optimized for use in sidebars, particularly in macOS or iPadOS apps, where the list acts as a navigation pane.

> **Default value:** `automatic`



```xml
<body>
  <list>
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/menu-0.png?ts=1735484869.719993" alt="Example" width="250"/>

---
*grouped List*

```xml
<body>
  <list listStyle="grouped">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/menu-1.png?ts=1735484869.719995" alt="Example" width="250"/>

---
*insetGrouped List*

```xml
<body>
  <list listStyle="insetGrouped">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/menu-2.png?ts=1735484869.719996" alt="Example" width="250"/>

---
*List with sections*

```xml
<body>
  <list>
  	<section header="Section 1 Header" footer="Section 1 Footer">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
    </section>
    
    <section header="Section 2 Header" footer="Section 2 Footer">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
    </section>
  </list>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/menu-3.png?ts=1735484869.719998" alt="Example" width="250"/>

---
