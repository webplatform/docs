---
title: Connection
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Provides a handle to the device''s connection information.'
tags:
  0: API
  1: Objects
  3: Mobile
  4: Network
  5: Information
uri: 'apis/network information/Connection'

---
## <span>Summary</span>

Provides a handle to the device's connection information.

## <span>Properties</span>

API Name
:   Summary

[bandwidth](/apis/network_information/Connection/bandwidth)
:   An estimation of the current bandwidth in MB/s (Megabytes per seconds) available.

[metered](/apis/network_information/Connection/metered)
:   A connection is metered when the user's connection is subject to a limitation from his Internet Service Provider strong enough to request web applications to be careful with the bandwidth usage.

[onchange](/apis/network_information/Connection/onchange)
:   Handles the change event, fired when the Connection changes.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

API Name
:   Summary

[change](/apis/network_information/Connection/change)
:   Fires when the Connection changes.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## <span>Related specifications</span>

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
