# ExtendedList

**Description**

A list view with added functionality like search and content unavailable states.

**Parameters**

- `dataModel`: The name of the data model to display in the list.
- `searchable`: A dictionary defining the search behavior (e.g., `mode`, `keys`, `allMustMatch`, `caseSensitive`).
- `reversed`: A boolean indicating whether to reverse the order of the list.
- `maxLimit`: The maximum number of items to display.
- `contentUnavailable`: The `id` of a view to display when the list is empty.

**Example**

```xml
<body>
    <extendedlist dataModel="myItems" searchable="mode:contains;keys:[name]" contentUnavailable="noItemsView"/>
    <contentunavailableview id="noItemsView" title="No Items" description="There are no items to display."/>
</body>
```

<img src="/Screenshots/Views/Custom/extendedlist_1.png" width="250" alt="Screenshot">
