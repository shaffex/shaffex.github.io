**ContentUnavailableView** is a view that you can use to indicate that content is not available. This view is typically used when there is no data to display or when an error has occurred that prevents content from being shown. It provides a standardized way to inform users that the expected content cannot be displayed.

***Parameters:***

`title` Text view that provides the main message to the user.

`description` (optional) Text view that provides additional context or instructions.

`systemImage` (optional) An optional system Image view that can be used to visually represent the unavailability of content.

## Examples

*If no systemImage provided*

```xml
<body>  
  <contentunavailableview title="Title" description="Description">
  </contentunavailableview>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/contentunavailableview-0.png?ts=1735484869.720148" alt="Example" width="250"/>

---
*If no systemImage provided*

```xml
<body>  
  <contentunavailableview title="Title" description="Description" systemImage="exclamationmark.triangle">
  </contentunavailableview>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/contentunavailableview-1.png?ts=1735484869.72015" alt="Example" width="250"/>

---
