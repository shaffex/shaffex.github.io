# DisclosureGroup

**Description**

A view that shows or hides another content view, based on the state of a disclosure control.

**Parameters**

- `header`: The text to display as the header of the disclosure group.
- `key`: A binding to a Boolean value that determines whether the group is expanded.
- `value`: The initial state of the disclosure group (true for expanded, false for collapsed).

**Example**

```xml
<body>
    <list>
        <disclosuregroup header="Section 1" key="isExpanded1" value="true">
            <text>Item 1</text>
            <text>Item 2</text>
        </disclosuregroup>
        <disclosuregroup header="Section 2" key="isExpanded2" value="false">
            <text>Item 3</text>
            <text>Item 4</text>
        </disclosuregroup>
    </list>
</body>
```
<img src="/Screenshots/Views/Controls/disclosuregroup_1.png" width="250" alt="Screenshot">
