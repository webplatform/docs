---
title: 'NetworkInformation'
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Is exposed on the Navigator object, and all instances of the Navigator type are defined to also implement the NetworkInformation interface.'
tags:
  - API_Objects
  - API
  - Mobile
  - Network_Information
uri: 'apis/network information/NetworkInformation'

---
## Summary

Is exposed on the Navigator object, and all instances of the Navigator type are defined to also implement the NetworkInformation interface.

## Properties

[connection](/apis/network_information/NetworkInformation/connection)
:   The object from which connection information is accessed.

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` js
function show() {
  console.log(navigator.connection.bandwidth);
}

navigator.connection.addEventListener('change', show, false);

show();
```

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
