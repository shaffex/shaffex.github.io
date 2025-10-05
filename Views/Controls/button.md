**Button** is a user interface component that triggers an action when tapped by the user. It can display text, an icon, or both, and it's highly customizable.
In SwiftUI, a Button is a user interface control that performs an action when tapped by the user. It can contain text, an image, or both, and you can customize its appearance and behavior.

***Parameters:***

`action`  is the action executed when the button is tapped. For more details see [Actions](./Actions.md)

`role` (optional)  is used to semantically indicate the purpose of a button, such as whether it performs a destructive action or is a cancel button. This semantic information can be used by the system to adjust the button's appearance accordingly and to provide appropriate accessibility features.
* `none` Default button behaviour
* `destructive` Indicates that the action performed by the button is irreversible or could lead to data loss. This role is used to warn users about the potential consequences of their action. The system may also use this semantic information to style the button accordingly, often with a red color, to signal its destructive nature to the user.
* `cancel` Indicates that the action performed by the button will dismiss a view or cancel the current operation without making any changes. This role is particularly useful in dialogues or modal views where you have actions like "Cancel" or "Dismiss" that allow the user to opt-out of a process without proceeding further. The system may use this semantic information to style the button appropriately or to handle the button action in a way that's consistent with cancel operations across the OS.

> **Note:** If you don't specify any `role`, default value is `none`

## Examples

*Confirmation dialog with positive, destructive and cancel buttons*

```xml
<body>
    <vstack confirmationDialog="isPresented:myConfirmationDialog" onAppear="presentConfirmationDialog:isPresented:myConfirmationDialog"/>
    <alert id="myConfirmationDialog" alertTitle="Confirmation Dialog" alertMessage="Can you see positive, destructive and cancel buttons?">
        <button role="">Positive</button>
        <button role="destructive">Destructive</button>
        <button role="cancel">Cancel</button>
    </alert>
</body>
```
<img src="/Screenshots/Views/Controls/button_1.png" width="250" alt="Screenshot">


---
*123*

```xml
<body>
    <button>Press Me 2</button>
</body>
```
<img src="/Screenshots/Views/Controls/button_2.png" width="250" alt="Screenshot">


---
*Button with custom view*

```xml
<body>
    <vstack>
        <button>
            <vstack padding="" background="red" clipShape="capsule" foregroundColor="white">
                <image systemName="plus" font="largeTitle"/>
                <text>My custom button</text>
            </vstack>
        </button>
        <button padding="" background="red" clipShape="circle">
            <vstack foregroundColor="white">
                <image systemName="plus" font="largeTitle"/>
            </vstack>
        </button>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Controls/button_3.png" width="250" alt="Screenshot">


---
*Button with role*

```xml
<body>
    <vstack alert="isPresented:myAlert" onAppear="presentAlert:isPresented:myAlert">
        <button>Default Button</button>
        <button role="destructive">destructive Button</button>
        <button role="cancel">cancel Button</button>
        <text>Note: cancel role is in bold in alerts etc</text>
    </vstack>
    <alert id="myAlert" alertTitle="Warning" alertMessage="Do you want to delete all files?">
        <button role="destructive">Destructive</button>
        <button role="cancel">Cancel</button>
    </alert>
</body>
```
<img src="/Screenshots/Views/Controls/button_4.png" width="250" alt="Screenshot">


---
*Alert with cancel and destructive buttons*

```xml
<body>
    <emptyview alert="isPresented:myAlert" onAppear="presentAlert:isPresented:myAlert">
	</emptyview>
    <alert id="myAlert" alertTitle="Warning" alertMessage="Do you want to delete all files?">
        <button role="destructive">Destructive</button>
        <button role="cancel">Cancel</button>
    </alert>
</body>
```
<img src="/Screenshots/Views/Controls/button_5.png" width="250" alt="Screenshot">


---
*Button with buttonStyle*

```xml
<body>
    <vstack>
        <button>Default Button</button>
        <button buttonStyle="plain">plain Button</button>
        <button buttonStyle="bordered">bordered Button</button>
        <button buttonStyle="borderless">borderless Button</button>
        <button buttonStyle="borderedProminent">borderedProminent Button</button>
    </vstack>
</body>
```
<img src="/Screenshots/Views/Controls/button_6.png" width="250" alt="Screenshot">


---
