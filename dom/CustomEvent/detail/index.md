---
title: detail
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Retrieves additional information about an event.'
uri: dom/CustomEvent/detail

---
# detail

## Summary

Retrieves additional information about an event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CustomEvent](/dom/CustomEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var eventDetails = event.detail;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

The content of this property is user-defined. It can be an integer, date, array, or other object type.

## Examples

``` {.js}
function getCustomEventDetail(e) {
//retrieve detail for custom event
var customEventDetail = e.detail;
return customEventDetail;
}
```

## Usage

     Use this property to retrieve any available additional information about this developer-generated custom event. Note: It may be empty.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

