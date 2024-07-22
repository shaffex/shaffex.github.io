## Controls
<details markdown="block">
<summary>alert</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>sheet</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>fullScreenCover</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>actionSheet</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>

## Effects
<details markdown="block">
<summary>colorInvert</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.



```xml
<body>
<vstack>
    <zstack>
        <rectangle foregroundColor="red"/>
        <text>RED color</text>
    </zstack>
    
    <zstack>
        <rectangle foregroundColor="red" colorInvert=""/>
        <text>Inverted RED color</text>
    </zstack>
</vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/colorInvert-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>

## Layout
<details markdown="block">
<summary>frame</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>

## Text
<details markdown="block">
<summary>font</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.



```xml
<body>
    <list>

    <section header="Testing standard fonts">
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
    
    <section header="Testing color and font" footer="foregroundColor and font modifier">
        <text foregroundColor="red" font="body">RED body</text>
        <text foregroundColor="green" font="caption2">GREEN caption2</text>
        <text foregroundColor="blue" font="largeTitle">BLUE largeTitle</text>
    </section>
    
    <section header="System font" footer="System font is San Francisco Font">
        <text fontWeight="ultraLight">This is ultraLight text</text>
        
        <text font="size:30;weight:regular">This is regular text</text>
        <text font="size:30;weight:ultraLight">This is ultraLight text</text>
        <text font="size:30;weight:thin">This is thin text</text>
        <text font="size:30;weight:bold">This is bold text</text>
        <text font="size:30;weight:heavy">This is heavy text</text>
    </section>
    
    <section header="Custom font" footer="You can specify font name and font size&#13;Example:custom:Helvetica Neue,size:20">
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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/font-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>
