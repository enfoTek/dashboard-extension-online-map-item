A custom **Online Map** item allows you to place callouts on Google or Bing maps using geographical coordinates.

This dashboard item supports the [Master-Filtering](https://documentation.devexpress.com/#Dashboard/CustomDocument117060) feature.

## Installation

To add the Online Map dashboard item to the Web Dashboard, register a custom item extension in the Web Dashboard's [BeforeRender](https://documentation.devexpress.com/#Dashboard/DevExpressDashboardWebScriptsASPxClientDashboard_BeforeRendertopic) event.

```javascript
function onBeforeRender(sender) {
  var dashboardControl = sender.getDesigner();
  dashboardControl.registerExtension(new CustomItems.OnlineMapItemExtension(dashboardControl));
}
```

Note that Map JavaScript API applications require an authentication key of a certain provider. Use the dxMap's [key](https://js.devexpress.com/Documentation/16_2/ApiReference/UI_Widgets/dxMap/Configuration/key/) attribute to provide authentication keys.

For more information on authentication keys, see the required map provider documentation (e.g., [Google](https://developers.google.com/maps/documentation/javascript/get-api-key?hl=en) or [Bing](https://msdn.microsoft.com/en-us/library/ff428642.aspx)).


## Settings
The **Online Map** dashboard item supports the following settings that you can configure in the Wed Dashboard UI:
* **Provider** - Specifies whether to show Google or Bing maps.
* **Type** - Specifies the map type. You can choose between RoadMap, Satellite or Hybrid.
* **Display Mode** - Specifies whether to show markers or routes.
