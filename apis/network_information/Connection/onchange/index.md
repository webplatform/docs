---
title: onchange
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
  0: API
  1: Object
  2: Properties
  4: Mobile
  5: Network
  6: Information
uri: 'apis/network information/Connection/onchange'

---
## <span>Summary</span>

Handles the change event, fired when the Connection changes.

Property of [apis/network\_information/Connection](/apis/network_information/Connection)[apis/network\_information/Connection](/apis/network_information/Connection)

## <span>Syntax</span>

``` js
var result = connection.onchange;
connection.onchange = value;
```

## <span>Return Value</span>

Returns an object of type EventHandlerEventHandler

**Needs Examples**: This section should include examples.

## <span>Notes</span>

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## <span>Related specifications</span>

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
