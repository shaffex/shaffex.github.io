# Font

**Description**

`font` modifier is used to set the font of text-based views (like Text, TextField, Label, etc.) in your SwiftUI views. You can specify the size, weight, and style of the font using this modifier. The font modifier can take various parameters, including predefined text styles (like .title, .body, .caption, etc.) that automatically adjust to the user's preferred text size, or custom fonts where you specify the font name and size.

**Examples**

**Predefined system fonts**

```xml
<body>
    <list>
        <section header="Predefined system fonts">
            <text font="largeTitle">largeTitle</text>
            <text font="title">title</text>
            <text font="title2">title2</text>
            <text font="title3">title3</text>
            <text font="headline">headline</text>
            <text font="subheadline">subheadline</text>
            <text font="body">body</text>
            <text font="callout">callout</text>
            <text font="caption">caption</text>
            <text font="caption2">caption2</text>
            <text font="footnote">footnote</text>
        </section>
    </list>
</body>
```

<img src="/Screenshots/Modifiers/Text/font_1.png" width="250" alt="Screenshot">

**Font and colors**

```xml
<body>
    <list>
        <section header="Font and colors" footer="Various fonts with colors">
            <text foregroundColor="red" font="body">RED body</text>
            <text foregroundColor="green" font="caption2">GREEN caption2</text>
            <text foregroundColor="blue" font="largeTitle">BLUE largeTitle</text>
            <text foregroundColor="orange" font="custom:Courier;size:20">ORANGE Courier (20)</text>
        </section>
    </list>
</body>
```

<img src="/Screenshots/Modifiers/Text/font_2.png" width="250" alt="Screenshot">

**System font with size and weight**

```xml
<body>
    <list>
        <section header="System font with size and weight" footer="System font is San Francisco Font">
            <text fontWeight="ultraLight">This is ultraLight text</text>
            <text font="size:30;weight:regular">This is regular text</text>
            <text font="size:30;weight:ultraLight">This is ultraLight text</text>
            <text font="size:30;weight:thin">This is thin text</text>
            <text font="size:30;weight:bold">This is bold text</text>
            <text font="size:30;weight:heavy">This is heavy text</text>
        </section>
    </list>
</body>
```

<img src="/Screenshots/Modifiers/Text/font_3.png" width="250" alt="Screenshot">

**Custom font and size**

```xml
<body>
    <list>
        <section header="Custom font" footer="You can specify font name and font size
Example:custom:Helvetica Neue,size:20">
            <text font="custom:System;size:20">System (30)</text>
            <text font="custom:Helvetica Neue;size:20">Helvetica Neue (20)</text>
            <text font="custom:Helvetica Neue;size:24">Helvetica Neue (24)</text>
            <text font="custom:Verdana Italic;size:32">Verdana Itali (32)</text>
            <text font="custom:Courier;size:20">Courier (20)</text>
            <text font="custom:Arial;size:30">Arial (30)</text>
            <text font="custom:Georgia;size:30">Georgia (30)</text>
            <text font="custom:Nonexisting font;size:30">Nonexisting font (30)</text>
        </section>
    </list>
</body>
```

<img src="/Screenshots/Modifiers/Text/font_4.png" width="250" alt="Screenshot">
