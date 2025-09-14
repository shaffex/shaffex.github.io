# Alert

**Description**

Presents an alert when a given condition is true.

**Parameters**

- `isPresented`: A binding to a Boolean value that determines whether to present the alert.
- `item`: A binding to an optional identifiable item. When the item is not nil, the alert is presented.

**Examples**

```xml
<body>
<vstack>
  <button alert="isPresented:myAlert" action="presentAlert:isPresented:myAlert">presentAlert:isPresented:myAlert</button>
</vstack>

<alert id="myAlert" alertTitle="Info" alertMessage="This is my alert">
</alert>

</body>
```

```xml
<body>
<button alert="item:myAlertItem" action="presentAlert:item:myAlertItem;id:myAlert" onAppear="presentAlert:item:myAlertItem;id:myAlert">Show Alert</button>

<alert id="myAlert" alertTitle="Info" alertMessage="This is my alert">
</alert>

</body>
```
