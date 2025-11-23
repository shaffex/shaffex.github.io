TEST


```xml
<body>
    <vstack padding="">
        <lazyvgrid border="color:black;width:{{$gridWidth*2}}" spacing="0" columns="8" spacing2="0">
            <foreach dataModel="matrix8x8">
                <rectangle aspectRatio="fit" foregroundColor="$dataModel.p" contentShape="rectangle" border="color:black;width:$gridWidth" onTapGesture="selectItem:selectedItem\\editItem:dataModel:matrix8x8;p:pixelColor"/>
            </foreach>
        </lazyvgrid>
        <text bold="">Preview:</text>
        <lazyvgrid width="80" height="80" spacing="0" border="color:blue;width:1" columns="8" spacing2="0">
            <foreach dataModel="matrix8x8">
                <rectangle aspectRatio="fit" foregroundColor="$dataModel.p" contentShape="rectangle"/>
            </foreach>
        </lazyvgrid>
        <stepper key="gridWidth" value="0.5" range="from:0;to:1;step:0.25;type:double">Grid Width ($gridWidth)</stepper>
        <hstack>
            <customview src="predefinedColor" c="black"/>
            <customview src="predefinedColor" c="white"/>
            <customview src="predefinedColor" c="red"/>
            <customview src="predefinedColor" c="green"/>
            <customview src="predefinedColor" c="blue"/>
            <customview src="predefinedColor" c="yellow"/>
            <customview src="predefinedColor" c="orange"/>
            <customview src="predefinedColor" c="purple"/>
        </hstack>
        <colorpicker key="pixelColor" value="yellow">Select Color (current color: $pixelColor)</colorpicker>
        <button action="loadDataModel:dataModelName:matrix8x8;src:url:https://magic-ui.com/Examples/DataModels/pixel-data8x8.json">Clear</button>
    </vstack>
    <customview id="predefinedColor">
        <zstack>
            <button action="setColor:pixelColor=$c">
                <circle foregroundColor="$c"/>
            </button>
            <circle stroke="lineWidth:1" foregroundColor="primary"/>
        </zstack>
    </customview>
    <datamodel key="matrix8x8" type="json" src="url:https://magic-ui.com/Examples/DataModels/pixel-data8x8.json"/>
</body>
```
<img src="/Screenshots/Examples/PixelEditor_1.png" width="250" alt="Screenshot">
