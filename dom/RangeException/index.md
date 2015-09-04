---
title: RangeException
tags:
  - API
  - Objects
  - DOM
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - 'Missing code and message properties'
summary: 'Describes errors thrown by selection and range operations.'
uri: dom/RangeException

---
# RangeException

## Summary

Describes errors thrown by selection and range operations.

## Properties

API Name
:   Summary
[name](/dom/RangeException/name)
:   Returns a DOMString value that is the name of the error that occurred during a Range operation.

## Methods

*No methods.*

## Events

*No events.*

## Usage

     Use DOMException instead.

## Notes

Starting with Gecko 13.0 (Firefox 13.0 / Thunderbird 13.0 / SeaMonkey 2.10) the Range object throws a DOMException as defined in DOM 4, instead of a RangeException defined in prior specifications.

Gecko supported it up to Gecko 1.9, then removed it until Gecko 17 where it was reimplemented, matching the spec

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

Â

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#interface-range)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[RangeException Object](http://msdn.microsoft.com/en-us/library/ie/ff974358(v=vs.85).aspx) Article]

