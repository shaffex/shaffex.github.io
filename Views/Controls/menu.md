**Menu** is a control that reveals a list of actions when the user interacts with it.

***Parameters:***

*   `id`: A unique identifier for the menu.
*   `title`: The title of the menu, which is displayed as its label.
*   `systemImage`: The name of a system symbol to display next to the title.

***Example:***

The example below shows a `Menu` with the title "Menu". It contains several actions, including a nested submenu, buttons that perform actions like playing a system sound or opening a URL, and buttons with destructive and cancel roles. It also includes a `ControlGroup` with several buttons.

```xml
<body>
    <menu id="viewMenu" title="Menu">
        <text>Menu demo</text>
        <menu title="SubMenu">
            <button>Submenu Item</button>
            <controlgroup>
                <button>
                    <label systemImage="1.circle">Option 1</label>
                </button>
                <button>
                    <label systemImage="2.circle">Option 2</label>
                </button>
            </controlgroup>
        </menu>
        <button action="playSystemSound:1022">playSystemSound</button>
        <button action="openUrl:https://apple.com">Open magic-ui.com</button>
        <divider/>
        <button role="destructive" action="yourAction">
            <label systemImage="trash">Delete</label>
        </button>
        <button role="cancel" action="yourAction">
            <label systemImage="pencil">Edit</label>
        </button>
        <controlgroup>
            <button>
                <label systemImage="1.circle">Option 1</label>
            </button>
            <button>
                <label systemImage="2.circle">Option 2</label>
            </button>
            <button>
                <label systemImage="3.circle">Option 3</label>
            </button>
        </controlgroup>
    </menu>
</body>
```
<img src="/Screenshots/Views/Controls/menu_1.png" width="250" alt="Screenshot">
