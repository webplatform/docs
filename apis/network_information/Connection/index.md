---
title: 'Connection'
notes:
  - 'See remark in topic. This API is not defined anywhere outside of the Network Information API W3C Note [1]. Also, this form lacks the specifications template.'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Provides a handle to the device''s connection information.'
tags:
  - API_Objects
  - API
  - Mobile
  - Network_Information
  - Needs_Examples
uri: 'apis/network information/Connection'

---
## Summary

Provides a handle to the device's connection information.

## Properties

[bandwidth](/apis/network_information/Connection/bandwidth)
:   An estimation of the current bandwidth in MB/s (Megabytes per seconds) available.

[metered](/apis/network_information/Connection/metered)
:   A connection is metered when the user's connection is subject to a limitation from his Internet Service Provider strong enough to request web applications to be careful with the bandwidth usage.

[onchange](/apis/network_information/Connection/onchange)
:   Handles the change event, fired when the Connection changes.

## Methods

*No methods.*

## Events

[change](/apis/network_information/Connection/change)
:   Fires when the Connection changes.

## Notes

As of 25 June 2014:

-   Formal work on the [Network Information](http://www.w3.org/TR/netinfo-api/) spec has been stopped. The specification is now a W3C Note.
-   Both Chrome and Firefox have shipped Network Information under an experimental feedback channel.

## Related specifications

[The Network Information API](http://www.w3.org/TR/netinfo-api/)
:   W3C Note
