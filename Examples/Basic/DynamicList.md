TEST HELLO MAGIC UI

A minimal example demonstrating rendering a single text element.

```xml
<body>
    <list listStyle="plain">
        <foreach dataModel="countries">
            <hstack>
                <text font="largeTitle">$dataModel.flag</text>
                <vstack alignment="leading">
                    <text font="headline">$dataModel.country</text>
                    <text>$dataModel.capital</text>
                </vstack>
            </hstack>
        </foreach>
    </list>

    <datamodel key="countries" type="json" src="url:https://magic-ui.com/Examples/DataModels/countries.json"/>
</body>
```
<img src="/Screenshots/Examples/Basic/DynamicList_1.png" width="250" alt="Screenshot">
