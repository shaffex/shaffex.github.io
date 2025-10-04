# VideoView

**Description**

A view that plays a video from a URL or a file path. It provides controls for playback, volume, and appearance.

**Parameters**

- `src`: The source URL of the video. Can be a remote URL (e.g., `url:https://...`) or a local file.
- `key`: The name of a variable in the environment that holds the video `URL`.
- `videoGravity` (optional): Controls how the video is scaled to fit the view.
  - `resize`: Stretches the video to fill the view, potentially distorting it. (Default)
  - `resizeAspect`: Scales the video to fit within the view while maintaining its aspect ratio.
  - `resizeAspectFill`: Scales the video to fill the view while maintaining its aspect ratio. Some parts of the video may be clipped.
- `isPlaying` (optional): A Boolean that determines if the video should play automatically. Defaults to `true`.
- `isLooping` (optional): A Boolean that determines if the video should loop automatically. Defaults to `true`.
- `volume` (optional): A value between 0.0 and 1.0 that sets the video's volume. Defaults to `1.0`.
- `showsPlaybackControls` (optional): A Boolean that determines if the standard playback controls are visible. Defaults to `true`.

## Examples

### Basic Video Player

This example shows a simple video player that plays a remote video file.

```xml
<body>
    <videoview src="url:https://shaffex.com/MagicUiDemo/Resources/TestVideo.mp4" videoGravity="resizeAspect"/>
</body>
```

<img src="/Screenshots/Views/Custom/videoview_1.png" width="250" alt="Screenshot">


---

### Autoplaying Video without Controls

This example shows a video that autoplays in a loop without any visible playback controls, serving as a background video.

```xml
<body>
    <videoview src="url:https://shaffex.com/MagicUiDemo/Resources/TestVideo.mp4" videoGravity="resizeAspectFill" showsPlaybackControls="false" isLooping="true" volume="0.0"/>
</body>
```

<img src="/Screenshots/Views/Custom/videoview_2.png" width="250" alt="Screenshot">

---

### Video with Playback controlled by a Toggle

This example demonstrates how to control video playback using a `toggle` switch.

```xml
<body>
    <vstack spacing="20">
        <videoview src="url:https://shaffex.com/MagicUiDemo/Resources/TestVideo.mp4" videoGravity="resizeAspect" isPlaying="$playVideo" isLooping="false"/>
        <toggle key="playVideo" value="true">Play Video</toggle>
    </vstack>
</body>
```

<img src="/Screenshots/Views/Custom/videoview_3.png" width="250" alt="Screenshot">
---
