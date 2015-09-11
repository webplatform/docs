---
title: chargingTime
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
  0: API
  1: Object
  2: Properties
  4: Battery
  5: Status
  6: Mobile
uri: 'apis/battery status/BatteryManager/chargingTime'

---
## <span>Summary</span>

Represents the time remaining in seconds until the system's battery is fully charged.

Property of [apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)[apis/battery\_status/BatteryManager](/apis/battery_status/BatteryManager)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = battery.chargingTime;
```

## <span>Return Value</span>

Returns an object of type doubledouble

**Needs Examples**: This section should include examples.

