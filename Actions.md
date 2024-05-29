
My image:

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://shaffex.com/MagicUiDemo/Help/images/noob2.png)

---

## vstack

> SwiftUI view: **VStack**

**VStack** is a view that arranges its children in a vertical line. The alignment parameter determines how the views are aligned horizontally.

`alignment`: This optional parameter determines the horizontal alignment of the views within the VStack. It's of type HorizontalAlignment and can take the following values:

* `leading`: Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `center`: Aligns the views along the center.
* `trailing`: Aligns the views along the trailing edge, which is the right edge in left-to-right languages.

> **Note:** If you don't specify a value for alignment, the stack will default to center alignment.

`spacing`: This optional parameter determines the vertical spacing between the views. 

> **Note:** If you don't provide a value, the stack uses a default spacing.

---

## hstack

SwiftUI: HStack

![Badge Name](https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>)

HStack is a view that arranges its children in a horizontal line. The alignment parameter determines how the views are aligned vertically.

`alignment`: This optional parameter determines the vertical alignment of the views within the HStack. It's of type VerticalAlignment and can take the following values:

* `top`: Aligns the views along the top edge.
* `center`: Aligns the views along the center.
* `bottom`: Aligns the views along the bottom edge.

> **Note:** If you don't specify a value for alignment, the stack will default to center alignment.

`spacing`: This optional parameter determines the horizontal spacing between the views. 

> **Note:** If you don't provide a value, the stack uses a default spacing.

Examples:

```xml
<vstack>
  <circle foregroundColor="red"/>
</vstack>
```
![Simulator Screenshot - iPhone 15 - 2024-05-29 at 18 55 43](https://github.com/shaffex/shaffex.github.io/assets/89866617/f266d290-bf9f-436d-a832-4ee0a77b84e1)




---

## zstack

SwiftUI: ZStack

![iOS](https://img.shields.io/badge/iOS-13.0%2B-blue)
![iPadOS](https://img.shields.io/badge/iPadOS-13.0%2B-blue)
![macOS](https://img.shields.io/badge/macOS-10.15%2B-blue)
![Mac Catalyst](https://img.shields.io/badge/Mac%20Catalyst-13.0%2B-blue)
![tvOS](https://img.shields.io/badge/tvOS-13.0%2B-blue)
![watchOS](https://img.shields.io/badge/watchOS-6.0%2B-blue)
![visionOS](https://img.shields.io/badge/visionOS-1.0%2B-blue)

ZStack is a view that overlays its children in depth order, with the first item in the list at the bottom and the last item on top. 

`alignment`: This optional parameter determines the alignment of the views within the ZStack. It's of type Alignment and can take the following values:

* `center`: Aligns the views along the center.
* `leading`: Aligns the views along the leading edge, which is the left edge in left-to-right languages like English.
* `trailing`: Aligns the views along the trailing edge, which is the right edge in left-to-right languages.
* `top`: Aligns the views along the top edge.
* `bottom`: Aligns the views along the bottom edge.
* `topLeading`: Aligns the views along the top and leading edges.
* `topTrailing`: Aligns the views along the top and trailing edges.
* `bottomLeading`: Aligns the views along the bottom and leading edges.
* `bottomTrailing`: Aligns the views along the bottom and trailing edges.

> **Note:** If you don't specify a value for alignment, the stack will default to center alignment.

Unlike VStack and HStack, ZStack does not have a `spacing` parameter because its children are overlaid on top of each other, not arranged in a line.
