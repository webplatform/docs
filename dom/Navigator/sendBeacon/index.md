---
title: sendBeacon
tags:
  - API
  - Object
  - Methods
  - DOM
  - WebRTC
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page''s unload or affecting the performance of the navigation.'
uri: dom/Navigator/sendBeacon

---
# sendBeacon

## Summary

Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page's unload or affecting the performance of the navigation.

*Method of [dom/Navigator](/dom/Navigator)*

## Syntax

``` {.js}
var result = navigator.sendBeacon(url, data);
```

## Parameters

### url

 Data-typeÂ
:   any

 DOMString

### data

 Data-typeÂ
:   any

 Must be of one of the following types:

-   ArrayBufferView
-   Blob
-   DOMString
-   FormData

## Return Value

Returns an object of type Boolean.

Boolean

**Boolean**. Returns one of the following possible values:

Return value
:   Description
true
:   The HTTP data was queued for transfer.
false
:   The HTTP data was not queued for transfer.

Â

## Examples

This example queues data for the server on the pagehide event.

``` {.js}
function() {
  window.addEventListener('pagehide', logData, false);
  function logData() {
    navigator.sendBeacon(
      'https://putsreq.herokuapp.com/Dt7t2QzUkG18aDTMMcop',
       'Sent by a beacon!');
   }
}();
```

## Related specifications

Specification
:   Status
[Beacon](http://www.w3.org/TR/beacon/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from HTML5Rocks! [article](http://updates.html5rocks.com/2014/10/Send-beacon-data-in-Chrome-39)

