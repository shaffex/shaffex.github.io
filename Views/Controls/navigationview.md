**NavigationView** is a container view that provides a navigation interface for hierarchical content. It's used to manage a stack of views, allowing users to navigate to deeper levels of content and return.

**Note:** `NavigationView` is deprecated in iOS 16 and later. For new apps, or apps targeting newer OS versions, it is recommended to use `NavigationStack`.

***Parameters:***

*   `navigationTitle`: The title to display in the navigation bar.
*   `navigationTitleDisplayMode`: An attribute that controls how the navigation title is displayed. It can have one of the following values:
    *   `automatic`: The default mode, which typically displays a large title that transitions to an inline title as the user scrolls.
    *   `large`: Always displays a large title.
    *   `inline`: Always displays a smaller, inline title within the navigation bar.

***Example:***

The example below shows a `NavigationView` containing a `List`. The `navigationTitle` is set to "Navigation View". A `NavigationLink` within the list allows the user to navigate to a detail view.

```xml
<body>
    <navigationview>
        <list navigationTitle="Navigation View">
            <navigationlink destination="viewDetails">
                <text>Go to Details</text>
            </navigationlink>
        </list>
    </navigationview>
    <text id="viewDetails">Details</text>
</body>
```
<img src="/Screenshots/Views/Controls/navigationview_1.png" width="250" alt="Screenshot">

***Inline Title Example:***

This example demonstrates the use of `navigationTitleDisplayMode="inline"` to force the navigation title to always be displayed in the smaller, inline format.

```xml
<body>
    <navigationview>
        <list navigationTitle="Navigation View" navigationTitleDisplayMode="inline">
            <navigationlink destination="viewDetails">
                <text>Go to Details</text>
            </navigationlink>
        </list>
    </navigationview>
    <text id="viewDetails">Details</text>
</body>
```
<img src="/Screenshots/Views/Controls/navigationview_2.png" width="250" alt="Screenshot">
