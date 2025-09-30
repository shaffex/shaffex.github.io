RadialGradient in SwiftUI is a view that creates a radial gradient color transition from an inner point to an outer circular shape. It's used to fill or overlay views with a gradient that radiates from the center to the edges with two or more colors. The gradient can be customized by specifying the center, start radius, and end radius, allowing control over the gradient's focal point and spread.

***Parameters:***

`gradient` See the example to understand how to specify colors, along with center, startRadius, and endRadius for radial gradients. The center is specified in UnitPoint for positioning, while startRadius and endRadius are specified in points to determine the gradient's spread.



```xml
<body>
    <radialgradient gradient="colors:[red,green,blue];center:0.5,0.5;startRadius:50;endRadius:200">
    </radialgradient>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/radialgradient-0.png?ts=1735484869.720142" alt="Example" width="250"/>

---
