---
title: msFirstPaint
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces. Non-standard; deletion candidate'
summary: 'Deletion candidate.'
uri: apis/timing/properties/msFirstPaint
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/timing/objects/performanceTiming
    - apis/timing/properties/navigationStart

---
# msFirstPaint

## Summary

Deletion candidate.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/timing/objects/performanceTiming](/w/index.php?title=apis/timing/objects/performanceTiming&action=edit&redlink=1)</span></span>

## Syntax

``` {.js}
var result = element.msFirstPaint;
element.msFirstPaint = value;
```

## Examples

The following example shows how to calculate the time that is required to request the document before the document begins to display for the user.

    var oTiming = window.performance.timing;
    var iTimeMS = oTiming.msFirstPaint - oTiming.navigationStart;

## Notes

### Remarks

The value reported by the **msFirstPaint** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC). Windows Internet Explorer 9. This property is supported only for documents displayed in IE9 Standards mode. For more information, please see Defining Document Compatibility.

### Syntax

## See also

### Related pages (MSDN)

-   `performanceTiming`
-   `navigationStart`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

