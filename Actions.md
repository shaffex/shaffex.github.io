## Actions
<details markdown="block">
<summary>playSystemSound</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.



```xml
<body>
    <button action="playSystemSound:1009">playSystemSound3:1009</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/playSystemSound-0.png?ts=1722298830.8671942" alt="Example" width="250"/>

---

</details>
<details markdown="block">
<summary>playAudio</summary><br>

**playAudio** This actions play sounds from various sources: a URL, a local file, or an embedded resource.

*Play from URL*

```xml
<button action="playAudio:url:https://shaffex.com/MagicUiDemo/Resources/audio/LadyGaga.mp3">Play from url</button>
```



---
*Play from local file*

```xml
<button action="playAudio:file:test.mp3">Play from file</button>
```



---
*Play from resource file*

```xml
<button action="playAudio:resource:test.mp3">Play from resource</button>
```



---
*Example how to play audio from various source and how to copy audio from utl to file*

```xml
<body>
<vstack>
    <button action="playAudio:url:https://shaffex.com/MagicUiDemo/Resources/audio/LadyGaga.mp3">Play from url</button>
    <button action="playAudio:file:test.mp3">Play from file</button>
    <button action="playAudio:resource:test.mp3">Play from resource</button>
</vstack>

<files>
  <copy src="url:https://shaffex.com/MagicUiDemo/Resources/audio/LadyGaga.mp3" dst="test.mp3"/>
</files>

</body>
```



---

</details>
<details markdown="block">
<summary>setAudioSession</summary><br>

ZStack is a container that overlays its children, aligning them in both axes.


</details>
