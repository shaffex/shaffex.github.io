# Popover

**Description**

Presents a popover when a given condition is true.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the popover.
- `item`: A binding to an optional identifiable item. When the item is not nil, the popover is presented.

**Example**

```xml
<myView popover="isPresented:myPopover">
    <text>Popover content</text>
</myView>
```
