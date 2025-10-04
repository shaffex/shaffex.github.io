# Control Size

**Description**

Sets the size for controls like buttons, toggles, and pickers within this view.

**Parameters**

- `size`: The control size to apply.
  - `mini`: A very small control size.
  - `small`: A small control size.
  - `regular`: The default control size.
  - `large`: A large control size.
  - `extraLarge`: An extra large control size.

**Examples**

```xml
<body>
    <vstack padding="20" spacing="20" alignItems="leading">
        <text font="headline">Control Size with Bordered Buttons</text>
        <vstack alignItems="leading" spacing="10">
            <button controlSize="mini" buttonStyle="bordered">Mini</button>
            <button controlSize="small" buttonStyle="bordered">Small</button>
            <button controlSize="regular" buttonStyle="bordered">Regular</button>
            <button controlSize="large" buttonStyle="bordered">Large</button>
            <button controlSize="extraLarge" buttonStyle="bordered">Extra Large</button>
        </vstack>
        <divider/>
        <text font="headline">Control Size with Toggles</text>
        <vstack alignItems="leading">
            <toggle isOn="$myToggle" controlSize="mini">Mini Toggle</toggle>
            <toggle isOn="$myToggle" controlSize="small">Small Toggle</toggle>
            <toggle isOn="$myToggle" controlSize="regular">Regular Toggle</toggle>
            <toggle isOn="$myToggle" controlSize="large">Large Toggle</toggle>
            <toggle isOn="$myToggle" controlSize="extraLarge">Extra Large Toggle</toggle>
        </vstack>
    </vstack>
</body>
```

<img src="/Screenshots/Modifiers/Controls/controlSize_1.png" width="250" alt="Screenshot">
