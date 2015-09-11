---
title: NetworkInformation
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Is exposed on the Navigator object, and all instances of the Navigator type are defined to also implement the NetworkInformation interface.'
tags:
  0: API
  1: Objects
  3: Mobile
  4: Network
  5: Information
uri: 'apis/network information/NetworkInformation'

---
## <span>Summary</span>

Is exposed on the Navigator object, and all instances of the Navigator type are defined to also implement the NetworkInformation interface.

## <span>Properties</span>

API Name
:   Summary

[connection](/apis/network_information/NetworkInformation/connection)
:   The object from which connection information is accessed.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

``` js
function show() {
  console.log(navigator.connection.bandwidth);
}

navigator.connection.addEventListener('change', show, false);

show();
```

## <span>Notes</span>

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## <span>Related specifications</span>

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
