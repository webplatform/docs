---
title: 'msFirstPaint'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces. Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/timing/objects/performanceTiming
    href: '/w/index.php?title=apis/timing/objects/performanceTiming&action=edit&redlink=1'
standardization_status: Non-Standard
summary: 'Deletion candidate.'
tags:
  - API_Object_Properties
  - API
  - Navigation_Timing
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/timing/objects/performanceTiming
    - apis/timing/properties/navigationStart
uri: apis/timing/properties/msFirstPaint

---
## Summary

Deletion candidate.

Property of [apis/timing/objects/performanceTiming](/w/index.php?title=apis/timing/objects/performanceTiming&action=edit&redlink=1)[apis/timing/objects/performanceTiming](/w/index.php?title=apis/timing/objects/performanceTiming&action=edit&redlink=1)

## Syntax

``` js
var result = element.msFirstPaint;
element.msFirstPaint = value;
```

## Examples

The following example shows how to calculate the time that is required to request the document before the document begins to display for the user.

``` html
var oTiming = window.performance.timing;
var iTimeMS = oTiming.msFirstPaint - oTiming.navigationStart;
```

## Notes

### Remarks

The value reported by the **msFirstPaint** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC). Windows Internet Explorer 9. This property is supported only for documents displayed in IE9 Standards mode. For more information, please see Defining Document Compatibility.

### Syntax

## See also

### Related pages

-   performanceTiming[performanceTiming](/w/index.php?title=apis/timing/objects/performanceTiming&action=edit&redlink=1)
-   navigationStart[navigationStart](/w/index.php?title=apis/timing/properties/navigationStart&action=edit&redlink=1)
