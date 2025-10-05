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
<img src="/Screenshots/Views/Other/contentunavailableview_1.png" width="250" alt="Screenshot">


---
*If no systemImage provided*

```xml
<body>
    <contentunavailableview title="Title" description="Description" systemImage="exclamationmark.triangle">
  </contentunavailableview>
</body>
```
<img src="/Screenshots/Views/Other/contentunavailableview_2.png" width="250" alt="Screenshot">


---
