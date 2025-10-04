# Dialog

**Description**

Presents a custom view as a modal dialog. The dialog appears on top of the current view, which is typically dimmed. This modifier is useful for alerts, pop-ups, or any custom modal interface.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the dialog.
- `item`: A binding to an optional identifiable item. When the item is not nil, the dialog is presented.

**Examples**

**Presenting with isPresented**

```xml
<body>
    <vstack>
        <button dialog="isPresented:myDialog" action="presentDialog:isPresented:myDialog">Present Dialog</button>
    </vstack>
    <vstack id="myDialog" background="white" cornerRadius="10" padding="20" shadow="radius:10">
        <text>This is a custom dialog.</text>
        <button action="dismissDialog:isPresented:myDialog">Close</button>
    </vstack>
</body>
```

<img src="/Screenshots/Modifiers/Custom/dialog_1.png" width="250" alt="Screenshot">

**Presenting with item**

```xml
<body>
    <vstack>
        <button dialog="item:myDialogItem" action="presentDialog:item:myDialogItem;id:myDialogContent">Present Dialog with item</button>
    </vstack>
    <vstack id="myDialogContent" background="white" cornerRadius="10" padding="20" shadow="radius:10">
        <text>This is a custom dialog presented with an item.</text>
        <button action="dismissDialog:item:myDialogItem">Close</button>
    </vstack>
</body>
```

<img src="/Screenshots/Modifiers/Custom/dialog_2.png" width="250" alt="Screenshot">
