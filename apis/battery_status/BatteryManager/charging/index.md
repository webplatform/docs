---
title: 'charging'
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
    value: Boolean
    href: /apis/battery_status/BatteryManager
standardization_status: 'W3C Candidate Recommendation'
summary: 'Represents if the system''s battery is charging.'
tags:
  - API_Object_Properties
  - API
  - Battery_Status
  - Mobile
  - Needs_Examples
uri: 'apis/battery status/BatteryManager/charging'

---
## Summary

Represents if the system's battery is charging.

Property of [apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)[apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)

## Syntax

**Note**: This property is read-only.

``` js
var result = battery.charging;
```

## Return Value

Returns an object of type BooleanBoolean

