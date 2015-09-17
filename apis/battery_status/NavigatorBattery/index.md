---
title: 'NavigatorBattery'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The NavigatorBattery interface is exposed on the Navigator object.'
tags:
  - API_Objects
  - API
  - Battery_Status
  - Mobile
uri: 'apis/battery status/NavigatorBattery'

---
## Summary

The NavigatorBattery interface is exposed on the Navigator object.

## Properties

[battery](/apis/battery_status/NavigatorBattery/battery)
:   The object that exposes the battery status information.

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` js
navigator.battery.onlevelchange = function () {
  console.log(navigator.battery.level);
};

/* or alternatively */

navigator.battery.addEventListener('levelchange', function () {
  console.log(navigator.battery.level);
}, false);
```

## Related specifications

[Battery Status API](http://www.w3.org/TR/battery-status/)
:   W3C Last Call Working Draft
