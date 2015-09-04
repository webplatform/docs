---
title: metered
tags:
  0: API
  1: Object
  2: Properties
  4: Mobile
  5: Network
  6: Information
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
summary: 'A connection is metered when the user''s connection is subject to a limitation from his Internet Service Provider strong enough to request web applications to be careful with the bandwidth usage.'
uri: 'apis/network information/Connection/metered'

---
# metered

## Summary

A connection is metered when the user's connection is subject to a limitation from his Internet Service Provider strong enough to request web applications to be careful with the bandwidth usage.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/network\_information/Connection](/apis/network_information/Connection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = connection.metered;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

**Needs Examples**: This section should include examples.

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

Specification
:   Status
[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note

