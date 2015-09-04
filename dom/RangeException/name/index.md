---
title: name
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - "Depreciated?\nsee DOM/RangeException"
summary: 'Returns a DOMString value that is the name of the error that occurred during a Range operation.'
uri: dom/RangeException/name

---
# name

## Summary

Returns a DOMString value that is the name of the error that occurred during a Range operation.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/RangeException](/dom/RangeException)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var sErrName = rangeException.name;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The name of the specific RangeException that occured.

## Notes

### Remarks

Range exception also supports a code value. The following table shows the code associated with the specific RangeException:

Code value
:   Name value
1
:   BadBoundarypointsError
2
:   InvalidNodeTypeError

Â

### Syntax

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#interface-range)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[name Property](http://msdn.microsoft.com/en-us/library/ie/hh974331(v=vs.85).aspx) Article]

