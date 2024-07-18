

## Controls
<details markdown="block">
<summary>button</summary>
<br><br>VStack is a container that stacks its children vertically.

```xml
<body>
    <button>Press Me</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>datepicker</summary>
<br><br>datepicker is a container that stacks its children vertically.

```xml
<body>
    <form>
    	<datepicker key="myDate" value="20240822T173000Z">Select date</datepicker>
    	<datepicker key="myDatemiw" value="19770822T102030Z">Select date2</datepicker>
    </form>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/datepicker-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>link</summary>
<br><br>link is a container that stacks its children vertically.

```xml
<body>
    <link url="https://shaffex.gitbub.io">My Link</link>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/link-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>list</summary>
<br><br>list is a container that stacks its children vertically.

```xml
<body>
    <list>
        <text>Item 1</text>
    </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-0.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
    <list listStyle="grouped">
        <text>Item 1</text>
    </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-1.png" alt="KOKOCE ALT" width="250"/>


</details>

## Layout
<details markdown="block">
<summary>vstack</summary>
<br><br>**VStack** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.



> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the views.
> **Default value:** System default spacing

```xml
<body>
    <foreach repeatCount="8">
    <hstack>
        <rectangle foregroundColor="red"/>
        <rectangle foregroundColor="orange"/>
        <rectangle foregroundColor="red"/>
    </hstack>
    </foreach>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-0.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
    <vstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>
    </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-1.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
  <vstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-2.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
  <hstack>
      <rectangle foregroundColor="yellow"/>
      <vstack>
          <rectangle foregroundColor="red"/>
          <rectangle foregroundColor="green"/>
          <rectangle foregroundColor="blue"/>
      </vstack>
      <rectangle foregroundColor="yellow"/>
  </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/vstack-3.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>hstack</summary>
<br><br>HStack is a container that stacks its children vertically.

```xml
<body>
    <hstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green"/>
        <circle foregroundColor="blue"/>        
    </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-0.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
  <hstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-1.png" alt="KOKOCE ALT" width="250"/>

```xml
<body>
  <vstack>
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-2.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>zstack</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <zstack>
        <circle foregroundColor="red"/>
        <circle foregroundColor="green" padding="50"/>
        <circle foregroundColor="blue"  padding="50"/>
    </zstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/zstack-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>lazyvgrid</summary>
<br><br>**LazyVGrid** is a view that arranges its children in a grid with flexible vertical rows. The alignment and spacing parameters determine how the views are aligned and spaced.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the LazyVGrid. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.
> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the rows in the grid.
> **Default value:** System default spacing

`columns` (optional) This parameter determines the grid structure. It's an array of GridItem objects that describe the layout of the grid's columns.

`gridItems` (optional) This parameter determines the grid structure. It's an array of GridItem objects that describe the layout of the grid's columns.
* `adaptive` text `minimum` `maximum` `spacing` `alignment`
* `flexible` text
* `fixed` text


> **Note:** You need to specify columns or gridItems


</details>
<details markdown="block">
<summary>geometryreader</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
<geometryreader proxy="geoProxy">

<zstack>
    <hstack spacing="0">
        
        <rectangle foregroundColor="red" width="{{$geoProxy.width*0.1}}"/>
        <rectangle foregroundColor="yellow" width="{{$geoProxy.width*0.2}}"/>
        <rectangle foregroundColor="red" width="{{$geoProxy.width*0.1}}"/>
        <rectangle foregroundColor="yellow" width="{{$geoProxy.width*0.2}}"/>
        <rectangle foregroundColor="red" width="{{$geoProxy.width*0.1}}"/>
        <rectangle foregroundColor="yellow" width="{{$geoProxy.width*0.2}}"/>
        <rectangle foregroundColor="red" width="{{$geoProxy.width*0.1}}"/>
        
    </hstack>

    <text font="largeTitle" background="blue">$geoProxy.width x $geoProxy.height</text>
</zstack>
</geometryreader>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/geometryreader-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>viewthatfits</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
<viewthatfits>
    <text font="largeTitle">This text should fit in landscape mode</text>
    <text >This text should fit in portrait mode</text>
</viewthatfits>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/viewthatfits-0.png" alt="KOKOCE ALT" width="250"/>


</details>

## Paint
<details markdown="block">
<summary>lineargradient</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <lineargradient gradient="colors:[red,green,blue];startPoint:0.0,0.5;endPoint:1.0,0.5">
    </lineargradient>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/lineargradient-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>radialgradient</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <radialgradient gradient="colors:[red,green,blue];center:0.5,0.5;startRadius:50;endRadius:200">
    </radialgradient>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/radialgradient-0.png" alt="KOKOCE ALT" width="250"/>


</details>

## Others

## Custom
<details markdown="block">
<summary>scrollingtext</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <vstack background="red">
    <scrollingtext>Scrolling text</scrollingtext>
    </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/scrollingtext-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>webview</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <webview xignoresSafeArea="" xopacity="0.5">string:b64:PGh0bWw+CiAgICA8aGVhZD4KICAgIAogICAgPG1ldGEgY2hhcnNldD0iVVRGLTgiPgogICAgPG1ldGEgbmFtZT0idmlld3BvcnQiIGNvbnRlbnQ9IndpZHRoPWRldmljZS13aWR0aCwgaW5pdGlhbC1zY2FsZT0xLjAiPgogICAgCiAgICAgICAgPHN0eWxlPgogICAgICAgICAgICBib2R5IHsKICBtYXJnaW46IDA7Cgp9CiAgICAgICAgPC9zdHlsZT4KCiAgICAgICAgCiAgICA8L2hlYWQ+CgogICAgCgogICAgPGNhbnZhcyBpZD0iY2FudiIvPgoKICAgIDxzY3JpcHQ+CiAgICAgICAgY29uc3QgY2FudmFzID0gZG9jdW1lbnQuZ2V0RWxlbWVudEJ5SWQoJ2NhbnYnKTsKY29uc3QgY3R4ID0gY2FudmFzLmdldENvbnRleHQoJzJkJyk7Cgpjb25zdCB3ID0gY2FudmFzLndpZHRoID0gZG9jdW1lbnQuYm9keS5vZmZzZXRXaWR0aDsKY29uc3QgaCA9IGNhbnZhcy5oZWlnaHQgPSBkb2N1bWVudC5ib2R5Lm9mZnNldEhlaWdodDsKY29uc3QgY29scyA9IE1hdGguZmxvb3IodyAvIDIwKSArIDE7CmNvbnN0IHlwb3MgPSBBcnJheShjb2xzKS5maWxsKDApOwoKY3R4LmZpbGxTdHlsZSA9ICcjMDAwJzsKY3R4LmZpbGxSZWN0KDAsIDAsIHcsIGgpOwoKZnVuY3Rpb24gbWF0cml4ICgpIHsKY3R4LmZpbGxTdHlsZSA9ICcjMDAwMSc7CmN0eC5maWxsUmVjdCgwLCAwLCB3LCBoKTsKCmN0eC5maWxsU3R5bGUgPSAnIzBmMCc7CmN0eC5mb250ID0gJzE1cHQgbW9ub3NwYWNlJzsKCnlwb3MuZm9yRWFjaCgoeSwgaW5kKSA9PiB7CmNvbnN0IHRleHQgPSBTdHJpbmcuZnJvbUNoYXJDb2RlKE1hdGgucmFuZG9tKCkgKiAxMjgpOwpjb25zdCB4ID0gaW5kICogMjA7CmN0eC5maWxsVGV4dCh0ZXh0LCB4LCB5KTsKaWYgKHkgPiAxMDAgKyBNYXRoLnJhbmRvbSgpICogMTAwMDApIHlwb3NbaW5kXSA9IDA7CmVsc2UgeXBvc1tpbmRdID0geSArIDIwOwp9KTsKfQoKc2V0SW50ZXJ2YWwobWF0cml4LCA1MCk7CiAgICA8L3NjcmlwdD4KCjwvaHRtbD4=</webview>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/webview-0.png" alt="KOKOCE ALT" width="250"/>


</details>
<details markdown="block">
<summary>videoview</summary>
<br><br>ZStack is a container that overlays its children, aligning them in both axes.

```xml
<body>
    <videoview src="url:https://shaffex.com/MagicUiDemo/Resources/TestVideo.mp4" videoGravity="resizeAspect"/>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/videoview-0.png" alt="KOKOCE ALT" width="250"/>


</details>
