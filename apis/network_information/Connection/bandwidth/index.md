---
title: 'bandwidth'
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/network_information/Connection
    href: /apis/network_information/Connection
  return:
    predicate: 'Returns an object of type '
    value: double
    href: /apis/network_information/Connection
standardization_status: Non-Standard
summary: 'An estimation of the current bandwidth in MB/s (Megabytes per seconds) available.'
tags:
  0: API
  1: Object
  2: Properties
  4: Mobile
  5: Network
  6: Information
uri: 'apis/network information/Connection/bandwidth'

---
## Summary

An estimation of the current bandwidth in MB/s (Megabytes per seconds) available.

Property of [apis/network\_information/Connection](/apis/network_information/Connection)[apis/network\_information/Connection](/apis/network_information/Connection)

## Syntax

**Note**: This property is read-only.

``` js
var result = connection.bandwidth;
```

## Return Value

Returns an object of type doubledouble

Returns 0 if the user is currently offline, infinity if the bandwidth is unknown.

**Needs Examples**: This section should include examples.

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
