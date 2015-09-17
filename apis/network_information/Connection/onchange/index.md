---
title: 'onchange'
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
    value: EventHandler
    href: /apis/network_information/Connection
standardization_status: Non-Standard
summary: 'Handles the change event, fired when the Connection changes.'
tags:
  - API_Object_Properties
  - API
  - Mobile
  - Network_Information
  - Needs_Examples
uri: 'apis/network information/Connection/onchange'

---
## Summary

Handles the change event, fired when the Connection changes.

Property of [apis/network\_information/Connection](/apis/network_information/Connection)[apis/network\_information/Connection](/apis/network_information/Connection)

## Syntax

``` js
var result = connection.onchange;
connection.onchange = value;
```

## Return Value

Returns an object of type EventHandlerEventHandler

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
