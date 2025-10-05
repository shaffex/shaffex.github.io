**Slider** is a control that allows users to select a value from a continuous range by moving a thumb along a track. It is commonly used for adjusting numerical values in a user interface.

***Parameters:***

`range` (optional) Check code example for range values.



```xml
<body>
    <form>
        <section header="Default: Value=$mySlider" footer="Default is int and 0-1">
            <slider key="mySlider" value="1">Default Slider</slider>
        </section>
        <section header="Int: Value=$mySliderInt" footer="range=&quot;from:1;to:5;type:int&quot;">
            <slider key="mySliderInt" value="3" range="from:1;to:5;type:int">Int Slider</slider>
        </section>
        <section header="Double: Value=$mySliderDouble1" footer="range=&quot;from:0;to:1;type:double&quot;">
            <slider key="mySliderDouble1" value="0.25" range="from:0;to:1;type:double">Double Slider</slider>
        </section>
        <section header="Double: Value=$mySliderDouble2" footer="range=&quot;from:0;to:10;step:0.5;type:double&quot;">
            <slider key="mySliderDouble2" value="7" range="from:0;to:10;step:0.5;type:double">Double Slider</slider>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Views/Controls/slider_1.png" width="250" alt="Screenshot">


---
