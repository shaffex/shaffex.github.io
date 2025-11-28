**Picker** is a control used to select a value from a list of mutually exclusive values. It can be presented in various styles, such as a wheel, segmented control, or menu. The Picker is often used in forms or settings screens where users need to choose from a predefined set of options.

***Parameters:***

`key` Name of the variable that will store the selected value from the picker.

`value` Default selection value

`title` (optional) Picker title

## Examples



```xml
<body>
    <form>
        <section footer="Selected value: $myPicker">
            <picker title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="nlue">Blue</text>
            </picker>
        </section>
        <section footer="pickerStyle=&quot;segmented&quot;">
            <picker pickerStyle="segmented" title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="blue">Blue</text>
            </picker>
        </section>
        <section footer="pickerStyle=&quot;menu&quot;">
            <picker pickerStyle="menu" title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="blue">Blue</text>
            </picker>
        </section>
        <section footer="pickerStyle=&quot;navigationLink&quot;">
            <picker pickerStyle="navigationLink" title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="blue">Blue</text>
            </picker>
        </section>
        <section footer="pickerStyle=&quot;inline&quot;">
            <picker pickerStyle="inline" title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="blue">Blue</text>
            </picker>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Views/Controls/picker_1.png" width="250" alt="Screenshot">


---


```xml
<body>
    <form>
        <section footer="pickerStyle=&quot;wheel&quot;">
            <picker height="120" pickerStyle="wheel" title="Select Color" key="myPicker" value="green">
                <text tag="red">Red</text>
                <text tag="green">Green</text>
                <text tag="blue">Blue</text>
            </picker>
        </section>
        <section footer="pickerStyle=&quot;wheel&quot;">
            <picker pickerStyle="wheel" title="Select Day" key="myPickerDay" value="Monday">
                <text tag="Monday">Monday</text>
                <text tag="Tuesday">Tuesday</text>
                <text tag="Wednesday">Wednesday</text>
                <text tag="Thursday">Thursday</text>
                <text tag="Friday">Friday</text>
                <text tag="Saturday">Saturday</text>
                <text tag="Sunday">Sunday</text>
            </picker>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Views/Controls/picker_2.png" width="250" alt="Screenshot">


---
