---
title: 'Location'
attributions:
  - 'Facebook HTML5 Resource Center.'
readiness: 'Ready to Use'
summary: 'Geolocation lets you identify a user''s location by returning their latitude and longitude. Applications can use this to offer localized experiences such as driving directions, nearby points of interest, local deals, etc. In the past few years, smartphones with dedicated GPS chips have exploded in popularity.'
tags:
  - Tutorials
  - Geolocation
  - JavaScript
uri: tutorials/location

---
## Summary

Geolocation lets you identify a user's location by returning their latitude and longitude. Applications can use this to offer localized experiences such as driving directions, nearby points of interest, local deals, etc. In the past few years, smartphones with dedicated GPS chips have exploded in popularity.

Devices base location on a number of things, including

-   The user's internet access point or Wi-Fi connection
-   The user's phone operator's cell-tower locations
-   An Embedded GPS chip in the user's phone

## Detecting Support

Geolocation is supported by all modern browsers, including Chrome 5.0+, Firefox 3.5+, IE 9.0+, Opera 10.6+, Safari 5.0+, and smartphone platforms including iPhone 3.0+, Android 2.0+, Windows Mobile 7. For up-to-date compatibility support, check out [CanIUse.com](http://www.caniuse.com/#search=geolocation).

You can use the [Modernizr JavaScript library](http://www.modernizr.com/) to detect support for the geolocation API. For example,

    if (Modernizr.geolocation) {
      // geolocation is supported
    } else {
      // no  geolocation support available
    }

## Location Functions

Geolocation functions are exposed under the `geolocation` property of the global navigator object.

    navigator.geolocation.getCurrentPosition(callback_function, error_handler, PositionOptions_interface_object)

This will asynchronously fetch and pass the user's current location to the `callback_function`. The location is only provided via callback to the callback function. If user has not yet authorized your app, a permission info bar/dialog will be rendered to the user. Here's what it looks like:

![location infobar.png](//static.webplatform.org/7/7e/location_infobar.png)

![iphone location warning.png](//static.webplatform.org/8/88/iphone_location_warning.png)

![android location warning.png](//static.webplatform.org/6/6f/android_location_warning.png)

### Success callback function

When the user's location is available, your callback function will receive a bundle of information. It's passed `position`, with two properties including `coords` and `timestamp`.

|Property|Returned|Type|Description|Example data|
|:-------|:-------|:---|:----------|:-----------|
|coords.latitude|Always|double|decimal degrees|37.774929|
|coords.longitude|Always|double|decimal degrees|-122.419415|
|coords.accuracy|Always|double|meters|50|
|coords.altitude|Optional|double or null|meters|150|
|coords.altitudeAccuracy|Optional|double or null|meters|8|
|coords.heading|Optional|double or null|degrees, calculated based on previous position.|20|
|coords.speed|Optional|double or null|meters/second, calculated based on previous position.|10|
|timestamp|Optional|DOMTimeStamp|bound to the `Date` type|1314300437317|

### Error callback function

If there is an error while fetching location or user denied permission to your app, the `error_handler` callback function is called with the `PositionError` object with following properties.

|Property|Type|Description|
|:-------|:---|:----------|
|code|short|enumerated value: `error.PERMISSION_DENIED` (1), `error.POSITION_UNAVAILABLE` (2), `error.TIMEOUT` (3), or `error.UNKNOWN_ERROR` (0)|
|message|DOMString|not to be presented to the end user.|

### Control how the location is fetched

The optional parameter, `PositionOptions_interface_object`, provides more control over how location is fetched, timeout or cached location via the following three optional properties.

|Property|Type|Default|Description|
|:-------|:---|:------|:----------|
|enableHighAccuracy|boolean|false|true will seek exact location if device supports it, else coarse location.|
|timeout|long|none|the time in milliseconds before the request should time out. Note that this is calculated after user has allowed sharing location.|
|maximumAge|long|0|in milliseconds. If provided, function returns cached location if available in the [(current - maximumAge) to current] time window|

## Monitoring Location

This function is exactly like the `getCurrentPosition` function except that the callback function will be automatically called every time user's location changes. It's useful in a service like turn-by-turn direction. The interval is optimally defined by the browser and can't be changed.

    int navigator.geolocation.watchPosition(callback_function, error_handler, PositionOptions_interface_object)

Unlike `getCurrentPosition`, this function returns an integer value which can be used to cancel the watch process and stop invoking any callbacks by calling the `clearWatch` function. This is how you call the `clearWatch` function:

    navigator.geolocation.clearWatch(int watch_number)

## Additional Resources

-   [HTML5 Geolocation Demo](http://html5demos.com/geo)
-   [Dive Into HTML5: You are here (and so is everybody else)](http://diveintohtml5.info/geolocation.html)
