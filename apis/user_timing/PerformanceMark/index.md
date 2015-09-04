---
title: PerformanceMark
tags:
  0: API
  1: Objects
  3: User
  4: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Exposes marks created via the mark() method to the Performance Timeline.'
uri: 'apis/user timing/PerformanceMark'

---
# PerformanceMark

## Summary

Exposes marks created via the mark() method to the Performance Timeline.

## Properties

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

## Methods

*No methods.*

## Events

*No events.*

## Notes

Timestamps represent the number of milliseconds between the time the event occurred and midnight Januaray 1, 1970 (UTC).

## Related specifications

Specification
:   Status
[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

