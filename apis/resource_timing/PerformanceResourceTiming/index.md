---
title: 'PerformanceResourceTiming'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Includes all resources fetched from the networking layer by the current browsing context.'
tags:
  - API_Objects
  - API
  - Resource_Timing
uri: 'apis/resource timing/PerformanceResourceTiming'

---
## Summary

Includes all resources fetched from the networking layer by the current browsing context.

## Properties

[connectEnd](/apis/resource_timing/PerformanceResourceTiming/connectEnd)
:   Returns the time immediately after the user agent finishes establishing the connection to the server to retrieve the resource.

[connectStart](/apis/resource_timing/PerformanceResourceTiming/connectStart)
:   Returns the time immediately before the user agent starts establishing the connection to the server to retrieve the resource.

[domainLookupEnd](/apis/resource_timing/PerformanceResourceTiming/domainLookupEnd)
:   Returns the time immediately after the user agent finishes the domain name lookup for the resource.

[domainLookupStart](/apis/resource_timing/PerformanceResourceTiming/domainLookupStart)
:   Returns the time immediately before the user agent starts the domain name lookup for the resource.

[fetchStart](/apis/resource_timing/PerformanceResourceTiming/fetchStart)
:   Returns the time immediately before the user agent starts to fetch the resource.

[initiatorType](/apis/resource_timing/PerformanceResourceTiming/initiatorType)
:   Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.

[redirectEnd](/apis/resource_timing/PerformanceResourceTiming/redirectEnd)
:   Returns the time immediately after receiving the last byte of the response of the last redirect.

[redirectStart](/apis/resource_timing/PerformanceResourceTiming/redirectStart)
:   Returns the starting time of the fetch that initiates the redirect.

[requestStart](/apis/resource_timing/PerformanceResourceTiming/requestStart)
:   Returns the time immediately before the user agent starts requesting the resource from the server, or from relevant application caches or from local resources.

[responseEnd](/apis/resource_timing/PerformanceResourceTiming/responseEnd)
:   Returns the time immediately after the user agent finishes receiving the last byte of the resource from from relevant application caches or from local resources.

[responseStart](/apis/resource_timing/PerformanceResourceTiming/responseStart)
:   Returns the time immediately after the user agent receives the first byte of the response from the server, or from relevant application caches or from local resources.

[secureConnectionStart](/apis/resource_timing/PerformanceResourceTiming/secureConnectionStart)
:   Returns the time immediately before the user agent starts the handshake process to secure the current connection.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/#performanceresourcetiming)
:   W3C Candidate Recommendation
