---
title: onchange
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
summary: 'Handles the change event, fired when the Connection changes.'
uri: 'apis/network information/Connection/onchange'

---
# onchange

## Summary

Handles the change event, fired when the Connection changes.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/network\_information/Connection](/apis/network_information/Connection)</span></span>

## Syntax

``` {.js}
var result = connection.onchange;
connection.onchange = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">EventHandler</span></span>

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

