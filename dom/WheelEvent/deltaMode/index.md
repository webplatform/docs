---
title: deltaMode
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[WheelEvent](https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent) Article]'
  - 'Microsoft Developer Network: [[deltaMode Property](http://msdn.microsoft.com/en-us/library/ie/ff974798(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/WheelEvent
    href: /dom/WheelEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/WheelEvent
standardization_status: 'W3C Recommendation'
summary: 'Gets a value that indicates the unit of measurement for delta values.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/WheelEvent/deltaMode

---
## Summary

Gets a value that indicates the unit of measurement for delta values.

Property of [dom/WheelEvent](/dom/WheelEvent)[dom/WheelEvent](/dom/WheelEvent)

## Syntax

**Note**: This property is read-only.

``` js
var deltaMode = event.deltaMode;
```

## Return Value

Returns an object of type NumberNumber

One of the following values -

-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_PIXEL, or 0x00 (hex), or 0. The delta coordinates are pixel based (most common).
-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_LINE, or 0x01 (hex), or 1. The delta coordinates are line based (in form controls, for example).
-   [WheelEvent](/dom/WheelEvent).DOM\_DELTA\_PAGE, or 0x02 (hex), or 2. The delta coordinates are page based.

## Examples

The following example shows how to determine the deltaMode property of the WheelEvent. Note: to feature test for deltaMode you need to use the 'deltaMode' in event as 0 (false) is a valid WheelEvent constant.

``` js
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

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
