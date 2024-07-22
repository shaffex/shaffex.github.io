## Controls
<details markdown="block">
<summary>button</summary><br>

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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-0.png" alt="KOKOCE ALT" width="250"/>

---
*123*

```xml
<body>
    <button>Press Me 2</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-1.png" alt="KOKOCE ALT" width="250"/>

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
	
	<button  padding="" background="red" clipShape="circle">
		<vstack foregroundColor="white">
			<image systemName="plus" font="largeTitle"/>
		</vstack>
	</button>
	</vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-2.png" alt="KOKOCE ALT" width="250"/>

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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-3.png" alt="KOKOCE ALT" width="250"/>

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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-4.png" alt="KOKOCE ALT" width="250"/>

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

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/button-5.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>datepicker</summary><br>

datepicker is a container that stacks its children vertically.



```xml
<body>
    <form>
    	<datepicker key="myDate" value="20240822T173000Z">Select date</datepicker>
    	<datepicker key="myDatemiw" value="19770822T102030Z">Select date2</datepicker>
    </form>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/datepicker-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>label</summary><br>

**Label** is a view that combines a text view with an icon view, providing a user interface element that can display both text and an image side by side. It is commonly used to represent actions, content, or to communicate the status of something in a concise and visually informative way.

***Parameters:***

`systemImage` (optional) Name of the SF symbol

`name` (optional) Name of image embedded in assets



```xml
<body>
  <form>
    <label foregroundColor="orange">Label with no image</label>
    <label systemImage="car.fill">Label with system image</label>
    <label foregroundColor="orange" systemImage="car.fill">Label with system image</label>
    <label image="noob2-30x30">Label with custom image</label>
    
    <label labelStyle="titleOnly" systemImage="car.fill">Label with system image</label>
   </form>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/label-0.png" alt="KOKOCE ALT" width="250"/>

---
*Label with labelStyle*

```xml
<body>
  <list padding="">
    <section footer="no labelStyle provided">
      <label systemImage="car.fill">Label title</label>
    </section>
    
    <section footer="labelStyle=automatic">
      <label labelStyle="automatic" systemImage="car.fill">Label title</label>
    </section>
    
    <section footer="labelStyle=automatic (with red color)">
      <label foregroundColor="red" labelStyle="automatic" systemImage="car.fill">Label title</label>
    </section>
    
    <section footer="labelStyle=iconOnly">
      <label labelStyle="iconOnly" systemImage="car.fill">Label title</label>
    </section>
    
    <section footer="labelStyle=titleOnly">
      <label labelStyle="titleOnly" systemImage="car.fill">Label title</label>
    </section>
    
    <section footer="labelStyle=titleAndIcon">
      <label labelStyle="titleAndIcon" systemImage="car.fill">Label title</label>
    </section>
   </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/label-1.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>link</summary><br>

link is a view that creates a navigation link to a URL that you provide. It allows you to open web URLs or deep links into other apps from your SwiftUI app. When a user taps on a Link, the system opens the URL in the appropriate app. For web URLs, this typically means opening the URL in the default web browser.



```xml
<body>
    <link url="https://shaffex.github.io">Open URL</link>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/link-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>list</summary><br>

**List** is a container that presents rows of data arranged in a single column, similar to UITableView in UIKit but with a more declarative and simpler syntax. It's commonly used for displaying a collection of items in a structured format and supports features like selection, deletion, and reordering of items if needed.

***Parameters:***

`listStyle` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `automatic` The standard or default list style that automatically adapts to the current platform or theme.
* `plain` A simple, plain style that does not show separators between rows by default and does not indent rows.
* `grouped` This style groups items in sections, similar to the grouped style in UIKit's UITableView. It's often used with a Section view to create distinct groups of items.
* `inset` Provides an inset appearance to the list, with margins on the sides, giving it a card-like feel.
* `insetGrouped` Combines the inset style with grouped sections, offering a modern look with background and spacing around grouped items.
* `sidebar` Optimized for use in sidebars, particularly in macOS or iPadOS apps, where the list acts as a navigation pane.

> **Default value:** `automatic`



```xml
<body>
  <list>
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-0.png" alt="KOKOCE ALT" width="250"/>

---
*grouped List*

```xml
<body>
  <list listStyle="grouped">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-1.png" alt="KOKOCE ALT" width="250"/>

---
*insetGrouped List*

```xml
<body>
  <list listStyle="insetGrouped">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
  </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-2.png" alt="KOKOCE ALT" width="250"/>

---
*List with sections*

```xml
<body>
  <list>
  	<section header="Section 1 Header" footer="Section 1 Footer">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
    </section>
    
    <section header="Section 2 Header" footer="Section 2 Footer">
    <text>Item 1</text>
    <text>Item 2</text>
    <text>Item 3</text>
    <text>Item 4</text>
    <text>Item 5</text>
    </section>
  </list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/list-3.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>toggle</summary><br>

In SwiftUI, a Toggle is a control that allows users to toggle between a true or false state. It is visually represented as a switch that users can tap or swipe to change its state. The Toggle view takes a binding to a Boolean value, which it updates according to the user's interaction. It also requires a label, which is typically used to describe the purpose of the toggle.

*My Toggle*

```xml
<body>
  <form>
    <toggle key="myToggle" value="true">My Toggle2</toggle>
    <toggle key="myToggle2" value="false">My Toggle2</toggle>
   </form>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/toggle-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>

## Layout
<details markdown="block">
<summary>vstack</summary><br>

**VStac** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

***Parameters:***

`alignment` (optional) This parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:
* `leading` Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center` Aligns the views along the center.
* `trailing` Aligns the views along the trailing edge, which is the right edge in left-to-right languages.

> **Default value:** center

`spacing` (optional) This parameter determines the vertical spacing between the views.
> **Default value:** System default spacing

## Examples

*Example 1: How to pickup a Noob*

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

---


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

---


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

---
*Toto je priklad 4*

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

---

</details>
<details markdown="block">
<summary>hstack</summary><br>

**HStack** is a view that arranges its children in a horizontal line. The alignment parameter determines how the views are aligned vertically.

***Parameters:***

`alignment` (optional) This parameter determines the vertical alignment of the views within the HStack. It's of type VerticalAlignment and can take the following values:
* `top` Aligns the views along the top edge.
* `center` Aligns the views along the center.
* `bottom` Aligns the views along the bottom edge.
* `firstTextBaseline` Aligns the first line of text in each view along a common baseline.
* `lastTextBaseline` Aligns the last line of text in each view along a common baseline.

> **Default value:** center

`spacing` (optional) This parameter determines the horizontal spacing between the views.
> **Default value:** System default spacing

## Examples

*Hstack example*

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

---


```xml
<body>
  <hstack spacing="0">
      <rectangle foregroundColor="red"/>
      <rectangle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </hstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-1.png" alt="KOKOCE ALT" width="250"/>

---
*Example with various spacings*

```xml
<body>
  <vstack>
  
  <text>spacing 0:</text>
  <hstack spacing="0">
    <rectangle foregroundColor="red"/>
      <circle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </hstack>
  
  <text>spacing 20:</text>
  <hstack spacing="20">
    <rectangle foregroundColor="red"/>
    <circle foregroundColor="green"/>
    <rectangle foregroundColor="blue"/>
  </hstack>
  
  <text>spacing 100:</text>
  <hstack spacing="100">
    <rectangle foregroundColor="red"/>
    <circle foregroundColor="green"/>
    <rectangle foregroundColor="blue"/>
  </hstack>
  
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-2.png" alt="KOKOCE ALT" width="250"/>

---
*Example with various alignments*

```xml
<body>
  <vstack>
  
  <text>top alignment:</text>
  <hstack alignment="top">
    <rectangle foregroundColor="red"/>
      <circle foregroundColor="green"/>
      <rectangle foregroundColor="blue"/>
  </hstack>
  
  <text>center alignment:</text>
  <hstack alignment="center">
    <rectangle foregroundColor="red"/>
    <circle foregroundColor="green"/>
    <rectangle foregroundColor="blue"/>
  </hstack>
  
  <text>bottom alignment:</text>
  <hstack alignment="bottom">
    <rectangle foregroundColor="red"/>
    <circle foregroundColor="green"/>
    <rectangle foregroundColor="blue"/>
  </hstack>
  
  </vstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/hstack-3.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>zstack</summary><br>

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
        <circle foregroundColor="blue"  padding="100"/>
    </zstack>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/zstack-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>lazyvgrid</summary><br>

**LazyVGrid** is a view that arranges its children in a grid with flexible vertical rows. The alignment and spacing parameters determine how the views are aligned and spaced.

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
<summary>geometryreader</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>viewthatfits</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>

## Paint
<details markdown="block">
<summary>lineargradient</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.



```xml
<body>
    <lineargradient gradient="colors:[red,green,blue];startPoint:0.0,0.5;endPoint:1.0,0.5">
    </lineargradient>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/lineargradient-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>
<details markdown="block">
<summary>radialgradient</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.



```xml
<body>
    <radialgradient gradient="colors:[red,green,blue];center:0.5,0.5;startRadius:50;endRadius:200">
    </radialgradient>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/radialgradient-0.png" alt="KOKOCE ALT" width="250"/>

---

</details>

## Others

## Custom
<details markdown="block">
<summary>scrollingtext</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>webview</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
<details markdown="block">
<summary>videoview</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
