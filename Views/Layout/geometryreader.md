**GeometryReader** is a container view that provides access to the size and position of its child views. It allows you to read the geometry of the view hierarchy and use that information to adjust the layout dynamically.



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

<img src="https://magic-ui.com/Help/GitHubAssets/geometryreader-0.png?ts=1735484869.7201161" alt="Example" width="250"/>

---


```xml
<body>
<geometryreader proxy="geoProxy">

<zstack maxWidth="infinity" maxHeight="infinity">
    <circle foregroundColor="red" width="{{$geoProxy.width*0.8}}"/>
    <circle foregroundColor="green" width="{{$geoProxy.width*0.6}}"/>
    <circle foregroundColor="blue" width="{{$geoProxy.width*0.4}}"/>

    <vstack alignment="bottomLeading">
        <text foregroundColor="red" background="secondary">Red is 80%</text>
        <text foregroundColor="green" background="secondary">Green is 60%</text>
        <text foregroundColor="blue" background="secondary">Blue is 40%</text>
    </vstack>
</zstack>
</geometryreader>
</body>
```

<img src="https://magic-ui.com/Help/GitHubAssets/geometryreader-1.png?ts=1735484869.720118" alt="Example" width="250"/>

---
