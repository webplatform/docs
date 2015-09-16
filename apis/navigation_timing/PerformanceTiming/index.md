---
title: PerformanceTiming
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An interface that provides Web applications with timing-related information.'
tags:
  0: API
  1: Objects
  3: Navigation
  4: Timing
uri: 'apis/navigation timing/PerformanceTiming'

---
## Summary

An interface that provides Web applications with timing-related information.

## Properties

API Name
:   Summary

[connectEnd](/apis/navigation_timing/PerformanceTiming/connectEnd)
:   Returns the time immediately after the user agent finishes establishing the connection to the server to retrieve the current document.

[connectStart](/apis/navigation_timing/PerformanceTiming/connectStart)
:   Returns the time immediately before the user agent start establishing the connection to the server to retrieve the document.

[domComplete](/apis/navigation_timing/PerformanceTiming/domComplete)
:   Returns the time immediately before the user agent sets the current document readiness to "complete".

[domContentLoadedEventEnd](/apis/navigation_timing/PerformanceTiming/domContentLoadedEventEnd)
:   Returns the time immediately after the document's DOMContentLoaded event completes.

[domContentLoadedEventStart](/apis/navigation_timing/PerformanceTiming/domContentLoadedEventStart)
:   Returns the time immediately before the user agent fires the DOMContentLoaded event at the Document.

[domInteractive](/apis/navigation_timing/PerformanceTiming/domInteractive)
:   Returns the time immediately before the user agent sets the current document readiness to "interactive".

[domLoading](/apis/navigation_timing/PerformanceTiming/domLoading)
:   Returns the time immediately before the user agent sets the current document readiness to "loading".

[domainLookupEnd](/apis/navigation_timing/PerformanceTiming/domainLookupEnd)
:   Returns the time immediately after the user agent finishes the domain name lookup for the current document.

[domainLookupStart](/apis/navigation_timing/PerformanceTiming/domainLookupStart)
:   Returns the time immediately before the user agent starts the domain name lookup for the current document.

[fetchStart](/apis/navigation_timing/PerformanceTiming/fetchStart)
:   Returns the time immediately before the user agent starts checking any relevant application caches (if the resource is to be fetched using HTTP GET or equivalent). Otherwise, returns the time when the user agent starts fetching the resource.

[loadEventEnd](/apis/navigation_timing/PerformanceTiming/loadEventEnd)
:   Returns the time when the load event of the current document is completed, or returns zero when the load event is not fired or is not completed.

[loadEventStart](/apis/navigation_timing/PerformanceTiming/loadEventStart)
:   Returns the time immediately before the load event of the current document is fired, or returns zero when the load event is not fired yet.

[navigationStart](/apis/navigation_timing/PerformanceTiming/navigationStart)
:   Returns the time immediately after the user agent finishes prompting to unload the previous document. If there is no previous document, returns the same value as fetchStart.

[redirectEnd](/apis/navigation_timing/PerformanceTiming/redirectEnd)
:   Returns the time immediately after receiving the last byte of the response of the last redirect, if there are HTTP redirects or equivalent when navigating and all redirects and equivalents are from the same origin. Otherwise, returns zero.

[redirectStart](/apis/navigation_timing/PerformanceTiming/redirectStart)
:   Returns the starting time of the fetch that initiates the redirect, if there are HTTP redirects or equivalent when navigating and if all the redirects or equivalent are from the same origin,. Otherwise, returns zero.

[requestStart](/apis/navigation_timing/PerformanceTiming/requestStart)
:   Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.

[responseEnd](/apis/navigation_timing/PerformanceTiming/responseEnd)
:   Returns the time immediately after the user agent receives the last byte of the current document from the server, relevant application caches or from local resources, or immediately before the transport connection is closed, whichever comes first.

[responseStart](/apis/navigation_timing/PerformanceTiming/responseStart)
:   Returns the time immediately after the user agent receives the first byte of the response from the server, or from relevant application caches or from local resources.

[secureConnectionStart](/apis/navigation_timing/PerformanceTiming/secureConnectionStart)
:   Returns the time immediately before the user agent starts the handshake process to secure the current connection, if the scheme of the current page is HTTPS. If HTTPS is not used, returns zero.

[unloadEventEnd](/apis/navigation_timing/PerformanceTiming/unloadEventEnd)
:   Returns the time immediately after the user agent finishes the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document or the unload is not yet completed, returns zero.

[unloadEventStart](/apis/navigation_timing/PerformanceTiming/unloadEventStart)
:   Returns the time immediately before the user agent starts the unload event of the previous document. If there is no previous document or the previous document has a different origin than the current document, returns zero.

## Methods

*No methods.*

## Events

*No events.*

## Notes

When a webpage is displayed in Windows Internet Explorer 9 mode, Windows Internet Explorer records timestamps that correspond to the time when various steps occurred during the process used to load a document. Each property of the **performanceTiming** object corresponds to one of these timestamps. This object is not supported for Metro style apps using JavaScript. The built-in performance marks occur in the following order:

-   **navigationStart**
-   **redirectStart**
-   **unloadEventStart**
-   **unloadEventEnd**
-   **redirectEnd**
-   **fetchStart**
-   **domainLookupStart**
-   **domainLookupEnd**
-   **connectStart**
-   **connectEnd**
-   **requestStart**
-   **responseStart**
-   **responseEnd**
-   **domLoading**
-   **domInteractive**
-   **domContentLoadedEventStart**
-   **domContentLoadedEventEnd**
-   **domComplete**
-   **loadEventStart**
-   **loadEventEnd**
-   **msFirstPaint**

The properties of the **performanceTiming** object represent the number of milliseconds that have elapsed between midnight January 1, 1970 and the time the measurement was recorded.

## Related specifications

[W3C Navigation Timing Specification](http://w3c-test.org/webperf/specs/NavigationTiming/)
:   W3C Editor's Draft
