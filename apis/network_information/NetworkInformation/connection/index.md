---
title: connection
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/network_information/NetworkInformation
    href: /apis/network_information/NetworkInformation
  return:
    predicate: 'Returns an object of type '
    value: Connection
    href: /apis/network_information/NetworkInformation
standardization_status: Non-Standard
summary: 'The object from which connection information is accessed.'
tags:
  0: API
  1: Object
  2: Properties
  4: Mobile
  5: Network
  6: Information
uri: 'apis/network information/NetworkInformation/connection'

---
## Summary

The object from which connection information is accessed.

Property of [apis/network\_information/NetworkInformation](/apis/network_information/NetworkInformation)[apis/network\_information/NetworkInformation](/apis/network_information/NetworkInformation)

## Syntax

**Note**: This property is read-only.

``` js
var result = networkInformation.connection;
```

## Return Value

Returns an object of type ConnectionConnection

**Needs Examples**: This section should include examples.

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
