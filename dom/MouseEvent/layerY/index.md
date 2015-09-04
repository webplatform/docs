---
title: layerY
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Mixed
notes:
  - Reviewed
summary: "Returns the horizontal coordinate of the event relative to the current layer.\nlayerY is a non-standards property of the MouseEvent object.\n"
uri: dom/MouseEvent/layerY

---
# layerY

## Summary

Returns the horizontal coordinate of the event relative to the current layer. layerY is a non-standards property of the MouseEvent object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

``` {.js}
var result = element.layerY;
element.layerY = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The scaled value of the mouse X and Y positions relative to the positioned elements' client position. This may be an integer or double value depending on the viewport scale value.

## Examples

Microsoft added the layerY property to the MouseEvent in IE9 for Interoperability purposes, but recommends using the offsetY property instead. The example below uses feature testing to detect IE9 and higher emulation modes and uses the event.offsetX value. For webkit and gecko and IE8 and lower emulation modes, the event.layerY or the event.offsetY values are used instead.

``` {.js}
if(document.documentMode&&document.documentMode>=9){
  form.layerXCoords.value = evt.offsetX;
  form.layerYCoords.value = evt.offsetY;
  }
  else
  {
    form.layerXCoords.value = (evt.layerX)?evt.layerX:evt.offsetX;
    form.layerYCoords.value = (evt.layerY)?evt.layerY:evt.offsetY;
}
```

## Usage

     Determining the relative mouse position on scrollable web pages.

## Notes

### Remarks

A positioned element is an element whose position property is set to `relative`, `absolute` or `fixed`. For more information about element positioning, see About Element Positioning. **Note**  This property is provided for cross-browser compatibility. Use [**y**](/css/cssom/properties/y) instead.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[MDM event.layery](https://developer.mozilla.org/en-US/docs/Web/API/event.layerX) Article]

Portions of this content come from the Microsoft Developer Network: [[event.layery](http://msdn.microsoft.com/en-us/library/ie/gg130968(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[Using Multiple HTML5 canvases as layers](http://html5.litten.com/using-multiple-html5-canvases-as-layers/) article]

