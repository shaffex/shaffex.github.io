# Sheet

**Description**

Presents a sheet when a given condition is true.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the sheet.
- `item`: A binding to an optional identifiable item. When the item is not nil, the sheet is presented.

**Examples**

```xml
<body>
<vstack>
<button action="presentSheet:mySheet">presentSheet:mySheet</button>
<button sheet="isPresented:mySheet" action="presentSheet:isPresented:mySheet">presentSheet:isPresented:mySheet</button>
<button sheet="item:mySheetItem" action="presentSheet:item:mySheetItem;id:mySheet">presentSheet:item:mySheetItem;id:mySheet</button>
</vstack>

<vstack id="mySheet">
<text>I am new sheet</text>
<button sheet="isPresented:mySheet2" action="presentSheet:isPresented:mySheet2">presentSheet:isPresented:mySheet2</button>
</vstack>

<text id="mySheet2">I am new sheet 2</text>

</body>
```
