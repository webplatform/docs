---
title: deltaX
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Gets the distance that a mouse wheel has rotated around the x-axis (horizontal).'
uri: dom/WheelEvent/deltaX

---
# deltaX

## Summary

Gets the distance that a mouse wheel has rotated around the x-axis (horizontal).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/WheelEvent](/dom/WheelEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var deltaX = event.deltaX;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The X rotation distance in pixels, lines or pages.

## Examples

The following example shows how to determine the deltaX property of the WheelEvent. Note: to feature test for deltaX you need to use the 'deltaX' in event as deltaX may have a value of 0 (false)... (event.deltaX) can return false negatives.

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

## Notes

The measurement of the distance can be determined using the [deltaMode](/dom/WheelEvent/deltaMode) property.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[WheelEvent](https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent) Article]

Portions of this content come from the Microsoft Developer Network: [[deltaX Property](http://msdn.microsoft.com/en-us/library/ie/ff974799(v=vs.85).aspx) Article]

