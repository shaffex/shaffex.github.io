**Stepper** is a control that allows users to increment or decrement a value by tapping on a plus or minus button. It is commonly used for adjusting numerical values in a user interface.

***Parameters:***

`range` (optional) Check code example for range values.



```xml
<body>
  <form>
    <section header="Default: Value=$myStepper" footer="Default is int and 0-1">
    <stepper key="myStepper" value="1">Default Stepper</stepper>
    </section>

    <section header="Int: Value=$myStepperInt" footer='range="from:1;to:5;type:int"'>
    <stepper key="myStepperInt" value="3" range="from:1;to:5;type:int">Int Stepper</stepper>
    </section>

    <section header="Double: Value=$myStepperDouble" footer='range="from:0;to:10;step:0.5;type:double"'>
    <stepper key="myStepperDouble" value="3" range="from:0;to:10;step:0.5;type:double">Double Stepper</stepper>
    </section>
  </form>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/stepper-0.png?ts=1735484869.7200599" alt="Example" width="250"/>

---
