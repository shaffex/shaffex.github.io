## Actions
<details markdown="block">
<summary>playSystemSound</summary><br>

**playSystemSound**



```xml
<body>
    <button action="playSystemSound:1009">playSystemSound3:1009</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/playSystemSound-0.png?ts=1730849674.078329" alt="Example" width="250"/>

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

**setAudioSession**



```xml
<body>
<list>
    <picker title="Category" key="category" value="ambient">
        <text tag="ambient">ambient</text>
        <text tag="playback">playback</text>
        <text tag="multiRoute">multiRoute</text>
    </picker>

    <picker title="Mode" key="mode" value="moviePlayback">
        <text tag="spokenAudio">spokenAudio</text>
        <text tag="voiceChat">voiceChat</text>
        <text tag="moviePlayback">moviePlayback</text>
    </picker>

    <button font="footnote" action="setAudioSession:category:$category;mode:$mode">setAudioSession:category:$category;mode:$mode</button>

    <section>
        <button action="setAudioSessionIsActive:true">setAudioSessionIsActive:true</button>
        <button action="setAudioSessionIsActive:false">setAudioSessionIsActive:false</button>
    </section>
</list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/setAudioSession-0.png?ts=1730849674.078382" alt="Example" width="250"/>

---


```xml
<body>
<list>
    <button action="setAudioSession:category:ambient">setAudioSession:category:ambient</button>
	<button action="setAudioSession:category:multiRoute">setAudioSession:category:multiRoute</button>
	<button action="setAudioSession:category:playAndRecord">setAudioSessioncategory:playAndRecord</button>
	<button action="setAudioSession:category:playback">setAudioSession:category:playback</button>
</list>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/setAudioSession-1.png?ts=1730849674.078387" alt="Example" width="250"/>

---

</details>
<details markdown="block">
<summary>requestAuthorizationForNotifications</summary><br>

**playSystemSound** Hello Kokoce



```xml
<body>
    <button action="requestAuthorizationForNotifications">requestAuthorizationForNotifications</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/requestAuthorizationForNotifications-0.png?ts=1730849674.078404" alt="Example" width="250"/>

---


```xml
<body>
    <vstack>
    <button action="playSystemSound:1007">Test Sound</button>
    <button action="scheduleLocalNotification:id:MY_NOTIFICATION;timeInterval:60">Schedule Notification in 60 seconds</button>
    </vstack>
    
    <notification id="MY_NOTIFICATION">
        <title>Notification Title</title>
        <body>Notification Body</body>
        <sound>default</sound>
        <badge>1</badge>
    </notification>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/requestAuthorizationForNotifications-1.png?ts=1730849674.078409" alt="Example" width="250"/>

---

</details>
<details markdown="block">
<summary>scheduleLocalNotification</summary><br>

**scheduleLocalNotification** Hello Kokoce



```xml
<body>
    <vstack>
    <button action="playSystemSound:1007">Test Sound</button>
    <button action="scheduleLocalNotification:id:MY_NOTIFICATION;timeInterval:60">Schedule Notification in 60 seconds x</button>
    <button action="scheduleLocalNotification:id:NOTIFICATION_EVERY_60s;timeInterval:60;repeats:true">Every 60s</button>
    </vstack>
    
    <notification id="NOTIFICATION_EVERY_60s">
        <title>Scheduled evey 60s</title>
        <sound>default</sound>
    </notification>

    <notification id="MY_NOTIFICATION">
        <title>Notification Title</title>
        <body>Notification Body</body>
        <sound>default</sound>
        <badge>1</badge>
    </notification>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/scheduleLocalNotification-0.png?ts=1730849674.078426" alt="Example" width="250"/>

---

</details>
<details markdown="block">
<summary>cancelAllPendingNotifications</summary><br>

**cancelAllPendingNotifications** Hello Kokoce



```xml
<body>
    <button action="cancelAllPendingNotifications">cancelAllPendingNotifications</button>
</body>
```

<img src="https://shaffex.com/MagicUiDemo/Help/GitHubAssets/cancelAllPendingNotifications-0.png?ts=1730849674.07844" alt="Example" width="250"/>

---

</details>
