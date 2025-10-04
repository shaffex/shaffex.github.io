# Full Screen Cover

**Description**

Presents a view that covers the screen when a given condition is true.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the full screen cover.
- `item`: A binding to an optional identifiable item. When the item is not nil, the full screen cover is presented.

**Examples**

```xml
<body>
    <vstack>
        <button action="presentFullScreenCover:mySheet">presentFullScreenCover:mySheet</button>
        <button fullScreenCover="isPresented:mySheet" action="presentSheet:isPresented:mySheet">presentFullScreenCover:isPresented:mySheet</button>
        <button fullScreenCover="item:mySheetItem" action="presentFullScreenCover:item:mySheetItem;id:mySheet">presentFullScreenCover:item:mySheetItem;id:mySheet</button>
    </vstack>
    <vstack id="mySheet">
        <text>I am full screen cover</text>
        <button action="dismissFullScreenCover:mySheet">dismissFullScreenCover:mySheet</button>
        <button action="dismissFullScreenCover:isPresented:mySheet">dismissFullScreenCover:isPresented:mySheet</button>
        <button action="dismissFullScreenCover:item:mySheetItem">dismissFullScreenCover:item:mySheetItem</button>
    </vstack>
</body>
```

<img src="/Screenshots/Modifiers/Controls/fullScreenCover_1.png" width="250" alt="Screenshot">
