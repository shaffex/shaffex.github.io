**Form** is a container for grouping controls used for data entry. It provides a standard appearance and behavior for collecting user input, typically used in settings screens or data entry interfaces. Forms automatically apply appropriate styling to their child views based on the platform.

**Example**



```xml
<body>
    <form>
        <list navigationTitle="Form">
            <text>Item kkc</text>
            <text>Item 2</text>
            <text>macka</text>
            <text>Item 4</text>
            <text>Item 5</text>
        </list>
    </form>
</body>
```
<img src="/Screenshots/Views/Controls/form_1.png" width="250" alt="Screenshot">


---
*grouped List*

```xml
<body>
    <list listStyle="grouped">
        <text>Item 1</text>
        <text>Item 2</text>
        <text>Item 3</text>
        <text>noob 4</text>
        <text>Item 5</text>
    </list>
</body>
```
<img src="/Screenshots/Views/Controls/form_2.png" width="250" alt="Screenshot">


---
*insetGrouped List*

```xml
<body>
    <list listStyle="insetGrouped">
        <text>Item 1</text>
        <text>Item 2</text>
        <text>Item 3</text>
        <text>Item 4</text>
        <text>Item 5</text>
    </list>
</body>
```
<img src="/Screenshots/Views/Controls/form_3.png" width="250" alt="Screenshot">


---
*List with sections*

```xml
<body>
    <list>
        <section header="Section 1 Header" footer="Section 1 Footer">
            <text>Item 1</text>
            <text>Item 2</text>
            <text>Item 3</text>
            <text>Item 4</text>
            <text>Item 5</text>
        </section>
        <section header="Section 2 Header" footer="Section 2 Footer">
            <text>Item 1</text>
            <text>Item 2</text>
            <text>Item 3</text>
            <text>Item 4</text>
            <text>Item 5</text>
        </section>
    </list>
</body>
```
<img src="/Screenshots/Views/Controls/form_4.png" width="250" alt="Screenshot">


---
