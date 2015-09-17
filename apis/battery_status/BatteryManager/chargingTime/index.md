---
title: 'chargingTime'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/battery_status/BatteryManager
    href: /apis/battery_status/BatteryManager
  return:
    predicate: 'Returns an object of type '
    value: double
    href: /apis/battery_status/BatteryManager
standardization_status: 'W3C Candidate Recommendation'
summary: 'Represents the time remaining in seconds until the system''s battery is fully charged.'
tags:
  - API_Object_Properties
  - API
  - Battery_Status
  - Mobile
  - Needs_Examples
uri: 'apis/battery status/BatteryManager/chargingTime'

---
## Summary

Represents the time remaining in seconds until the system's battery is fully charged.

Property of [apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)[apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)

## Syntax

**Note**: This property is read-only.

``` js
var result = battery.chargingTime;
```

## Return Value

Returns an object of type doubledouble

