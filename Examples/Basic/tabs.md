## Tab based app

A minimal example demonstrating rendering a single text element.

```xml
<body>
    <tabview key="selectedTab" value="Home">
        <navigationstack tabItem="label:Home;systemImage:house" tag="Home">
            <text font="largeTitle">Home</text>
        </navigationstack>

        <navigationstack if="$isShowingSearch" tabItem="label:Search;systemImage:magnifyingglass" tag="Search">
            <text font="largeTitle">Search</text>
        </navigationstack>

        <navigationstack if="$isShowingFavorites" tabItem="label:Favorites;systemImage:heart.fill" tag="Favorites">
            <text font="largeTitle">Favorites</text>
        </navigationstack>

        <navigationstack if="$isShowingAlerts" tabItem="label:Alerts;systemImage:$alertImage" tag="Alerts" badge="$badgeText">
            <text font="largeTitle">Alerts</text>
        </navigationstack>

        <navigationstack tabItem="label:Settings;systemImage:gear" tag="Settings">
            <view src="viewSettings"/>
        </navigationstack>
    </tabview>

    <!-- Settings View -->
    <view id="viewSettings">
        <form navigationTitle="Settings">
            <toggle key="isShowingSearch" value="true">Search Tab</toggle>
            <toggle key="isShowingFavorites" value="true">Favorites Tab</toggle>

            <section>
                <toggle key="isShowingAlerts" value="true">Alerts Tab</toggle>

                <picker key="alertImage" value="bell" title="Alert Tab Icon">
                    <label tag="bell" systemImage="bell">bell</label>
                    <label tag="bell.circle" systemImage="bell.circle">bell.circle</label>
                    <label tag="bell.badge.fill" systemImage="bell.badge.fill">bell.badge.fill</label>
                </picker>

                <hstack>
                    <text>Badge Text</text>
                    <textfield key="badgeText" value="" multilineTextAlignment="trailing">t</textfield>
                </hstack>
                <button action="setString:badgeText=">Clear Badge Text</button>

            </section>

        </form>
    </view>

</body>
```
<img src="/Screenshots/Examples/Basic/tabs_1.png" width="250" alt="Screenshot">
