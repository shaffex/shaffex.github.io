# ProgressView

**Description**

A view that shows the progress of a task.

**Parameters**

- `key`: A binding to a numeric value that indicates the progress.
- `value`: The initial progress value.
- `range`: A dictionary specifying the range of the progress view (e.g., `from:0;to:100`).
- `progressViewStyle`: The style of the progress view. Can be `circular`, `linear`, or `automatic`.

**Example**

```xml
<body>
    <vstack spacing="20" padding="20">
        <progressview key="progress" value="0.75" range="from:0;to:1;type:double"/>
        <slider key="progress" value="0.75" range="from:0;to:1;type:double"/>
    </vstack>
</body>
```
