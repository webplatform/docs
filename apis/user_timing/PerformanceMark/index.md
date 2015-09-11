---
title: PerformanceMark
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Exposes marks created via the mark() method to the Performance Timeline.'
tags:
  0: API
  1: Objects
  3: User
  4: Timing
uri: 'apis/user timing/PerformanceMark'

---
## <span>Summary</span>

Exposes marks created via the mark() method to the Performance Timeline.

## <span>Properties</span>

API Name
:   Summary

[duration](/apis/user_timing/PerformanceMark/duration)
:   Returns a DOMHighResTimeStamp value. For marks, the value is always 0 (zero).

[entryType](/apis/user_timing/PerformanceMark/entryType)
:   Returns the DOMString "mark".

[name](/apis/user_timing/PerformanceMark/name)
:   Returns the mark's name.

[startTime](/apis/user_timing/PerformanceMark/startTime)
:   Returns a DOMHighResTimeStamp with the mark's High Resolution Time time value.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Notes</span>

Timestamps represent the number of milliseconds between the time the event occurred and midnight Januaray 1, 1970 (UTC).

## <span>Related specifications</span>

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Candidate Recommendation
