---
title: 'BatteryManager'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The object that exposes the battery status information.'
tags:
  - API_Objects
  - API
  - Battery_Status
  - Mobile
uri: 'apis/battery status/BatteryManager'

---
## Summary

The object that exposes the battery status information.

## Properties

[charging](/apis/battery_status/BatteryManager/charging)
:   Represents if the system's battery is charging.

[chargingTime](/apis/battery_status/BatteryManager/chargingTime)
:   Represents the time remaining in seconds until the system's battery is fully charged.

[dischargingTime](/apis/battery_status/BatteryManager/dischargingTime)
:   Represents the time remaining in seconds until the system's battery is completely discharged and the system is about to be suspended.

[level](/apis/battery_status/BatteryManager/level)
:   Represents the current battery level scaled from 0 to 1.0.

[onchargingchange](/apis/battery_status/BatteryManager/onchargingchange)
:   Handles the chargingchange event.

[onchargingtimechange](/apis/battery_status/BatteryManager/onchargingtimechange)
:   Handles the chargingtimechange event.

[ondischargingtimechange](/apis/battery_status/BatteryManager/ondischargingtimechange)
:   Handles the dischargingtimechange event.

[onlevelchange](/apis/battery_status/BatteryManager/onlevelchange)
:   Handles the levelchange event.

## Methods

*No methods.*

## Events

[chargingchange](/apis/battery_status/BatteryManager/chargingchange)
:   Fired when the battery charging state is updated.

[chargingtimechange](/apis/battery_status/BatteryManager/chargingtimechange)
:   Fired when the battery charging time is updated.

[dischargingtimechange](/apis/battery_status/BatteryManager/dischargingtimechange)
:   Fired when the battery discharging time is updated.

[levelchange](/apis/battery_status/BatteryManager/levelchange)
:   Fired when the battery level is updated.

## Related specifications

[Battery Status API](http://www.w3.org/TR/battery-status/)
:   W3C Last Call Working Draft
