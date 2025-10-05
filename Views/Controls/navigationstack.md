**NavigationStack** is a view that displays a root view and allows the user to navigate to subsequent views in a stack. It's the recommended way to manage navigation in SwiftUI for apps targeting iOS 16 and later, replacing the deprecated `NavigationView`.

`NavigationStack` provides a more flexible and powerful way to handle navigation, including programmatic navigation and deep linking.

***Parameters:***

*   `navigationTitle`: The title to display in the navigation bar.
*   `navigationTitleDisplayMode`: An attribute that controls how the navigation title is displayed. It can have one of the following values:
    *   `automatic`: The default mode, which typically displays a large title that transitions to an inline title as the user scrolls.
    *   `large`: Always displays a large title.
    *   `inline`: Always displays a smaller, inline title within the navigation bar.

***Example:***

The example below shows a `NavigationStack` containing a `List`. The `navigationTitle` is set to "Navigation Stack". A `NavigationLink` within the list allows the user to navigate to a detail view.

```xml
<body>
    <navigationstack>
        <list navigationTitle="Navigation Stack">
            <navigationlink destination="viewDetails">
                <text>Go to Details</text>
            </navigationlink>
        </list>
    </navigationstack>
    <text id="viewDetails">Details</text>
</body>
```
<img src="/Screenshots/Views/Controls/navigationstack_1.png" width="250" alt="Screenshot">

***Inline Title Example:***

This example demonstrates the use of `navigationTitleDisplayMode="inline"` to force the navigation title to always be displayed in the smaller, inline format.

```xml
<body>
    <navigationstack>
        <list navigationTitle="Navigation Stack" navigationTitleDisplayMode="inline">
            <navigationlink destination="viewDetails">
                <text>Go to Details</text>
            </navigationlink>
        </list>
    </navigationstack>
    <text id="viewDetails">Details</text>
</body>
```
<img src="/Screenshots/Views/Controls/navigationstack_2.png" width="250" alt="Screenshot">
