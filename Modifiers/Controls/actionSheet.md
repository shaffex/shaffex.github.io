# Action Sheet

**Description**

Presents an action sheet when a given condition is true.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the action sheet.
- `item`: A binding to an optional identifiable item. When the item is not nil, the action sheet is presented.

**Examples**

```xml
<body>
    <vstack actionSheet="isPresented:myActionSheet" onAppear="presentActionSheet:isPresented:myActionSheet"/>
    <alert id="myActionSheet" alertTitle="Action Sheet" alertMessage="Message for my action sheet">
        <button action="delay:0.01:presentActionSheet:isPresented:myActionSheet2">Open Action Sheet 2</button>
        <button>Action Default</button>
        <button role="destructive">Action Destructive</button>
        <button role="cancel">Action Cancel</button>
    </alert>
</body>
```

<img src="/Screenshots/Modifiers/Controls/actionSheet_1.png" width="250" alt="Screenshot">
