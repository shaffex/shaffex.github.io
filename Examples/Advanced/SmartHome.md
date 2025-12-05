# Smart Home Control Panel

A dashboard for managing smart home devices.

```xml
<body>
    <form>
        <section header="Living Room">
            <toggle key="livingRoomLights" value="true">Main Lights</toggle>
            <slider key="livingRoomBrightness" value="0.8" range="from:0;to:1;type:double">Brightness</slider>
            <picker title="Scene" key="livingRoomScene" value="relax">
                <text tag="relax">Relax</text>
                <text tag="party">Party</text>
                <text tag="movie">Movie</text>
            </picker>
        </section>
        <section header="Climate">
            <text>Temperature: $thermostatTemp</text>
            <slider key="thermostatTemp" value="22" range="from:16;to:30;step:0.5;type:double">Thermostat</slider>
            <toggle key="acPower" value="false">AC Power</toggle>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Examples/Advanced/SmartHome_1.png" width="250" alt="Screenshot">
