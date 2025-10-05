**ZStack** is a view that layers its children on top of each other, aligning them in both the horizontal and vertical axes. The alignment parameter determines how the views are aligned within the ZStack.


***Parameters:***

`alignment` (optional) This parameter determines the alignment of the views within the ZStack. It's of type Alignment and can take the following values:
* `topLeading` Aligns the views at the top leading corner.
* `top` Aligns the views along the top edge.
* `topTrailing` Aligns the views at the top trailing corner.
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views at the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.
* `bottomLeading` Aligns the views at the bottom leading corner.
* `bottom` Aligns the views along the bottom edge.
* `bottomTrailing` Aligns the views at the bottom trailing corner.

> **Default value:** center

*Example with circles in zstack*

```xml
<body>
    <zstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green" padding="50"/>
        <circle foregroundColor="blue" padding="100"/>
    </zstack>
</body>
```
<img src="/Screenshots/Views/Layout/zstack_1.png" width="250" alt="Screenshot">


---
