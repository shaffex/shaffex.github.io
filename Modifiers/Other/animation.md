# Animation

**Description**

Applies an animation to the view when a specified value changes.

**Parameters**

- `animation`: The animation to apply. Examples: `linear`, `easeIn`, `spring`.
- `duration`: The duration of the animation in seconds.
- `delay`: The delay before the animation starts.
- `value`: The value to monitor for changes to trigger the animation.

**Examples**

```xml
<body>
    <vstack>
        <text animation="animation:linear;duration:1;value:$myVar">Animate me</text>
        <button action="toggle:$myVar">Toggle</button>
    </vstack>
</body>
```

<img src="/Screenshots/Modifiers/Other/animation_1.png" width="250" alt="Screenshot">
