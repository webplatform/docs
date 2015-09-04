---
title: deltaMode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets a value that indicates the unit of measurement for delta values.'
uri: dom/WheelEvent/deltaMode

---
# deltaMode

## Summary

Gets a value that indicates the unit of measurement for delta values.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/WheelEvent](/dom/WheelEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var deltaMode = event.deltaMode;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

One of the following values -

-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_PIXEL, or 0x00 (hex), or 0. The delta coordinates are pixel based (most common).
-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_LINE, or 0x01 (hex), or 1. The delta coordinates are line based (in form controls, for example).
-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_PAGE, or 0x02 (hex), or 2. The delta coordinates are page based.

## Examples

The following example shows how to determine the deltaMode property of the WheelEvent. Note: to feature test for deltaMode you need to use the 'deltaMode' in event as 0 (false) is a valid WheelEvent constant.

``` {.js}
<script type="text/javascript">
function getDeltaMode(dMode){
    switch (dMode){
        case WheelEvent.DOM_DELTA_LINE:// 1
            return 'DOM_DELTA_LINE (1)';
        case WheelEvent.DOM_DELTA_PAGE:// 2
            return 'DOM_DELTA_PAGE (2)';
        case WheelEvent.DOM_DELTA_PIXEL:// 0
            return 'DOM_DELTA_PIXEL (0)';
        default:
            return 'Unknown DeltaMode:' + dMode;

    }
}
   function showWheelEvent(evt){
        if(!evt)evt=window.event;
        theform=document.forms.frmEvent;
        if(evt.type=='wheel'){
            theform.deltamode.value=('deltaMode' in evt)?getDeltaMode(evt.deltaMode):'N/A';
            theform.deltax.value=('deltaX' in evt)?evt.deltaX:'N/A';
            theform.deltay.value=('deltaY' in evt)?evt.deltaY:'N/A';
            theform.deltaz.value=('deltaZ' in evt)?evt.deltaZ:'N/A';
        }

   }
</script>
```

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[WheelEvent](https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent) Article]

Portions of this content come from the Microsoft Developer Network: [[deltaMode Property](http://msdn.microsoft.com/en-us/library/ie/ff974798(v=vs.85).aspx) Article]

