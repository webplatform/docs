---
title: NavigatorBattery
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The NavigatorBattery interface is exposed on the Navigator object.'
tags:
  0: API
  1: Objects
  3: Battery
  4: Status
  5: Mobile
uri: 'apis/battery status/NavigatorBattery'

---
## <span>Summary</span>

The NavigatorBattery interface is exposed on the Navigator object.

## <span>Properties</span>

API Name
:   Summary

[battery](/apis/battery_status/NavigatorBattery/battery)
:   The object that exposes the battery status information.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

``` js
navigator.battery.onlevelchange = function () {
  console.log(navigator.battery.level);
};

/* or alternatively */

navigator.battery.addEventListener('levelchange', function () {
  console.log(navigator.battery.level);
}, false);
```

## <span>Related specifications</span>

[Battery Status API](http://www.w3.org/TR/battery-status/)
:   W3C Last Call Working Draft
