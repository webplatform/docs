---
title: pressure
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.'
uri: dom/PointerEvent/pressure

---
# pressure

## Summary

The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var pressure = event.pressure;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">double</span></span>

Pressure of the pointer contact in range of 0 to 1.

## Examples

The following is an example of a pointermove event handler that outputs the value of the event.pressure property to a text field in a form (frmOutput);

``` {.js}
function getPressure(evt){
var theform=document.forms.frmOutput;
theform.txtPressure.value=evt.pressure;
}
```

## Usage

     Could be used for example to control the hue or opacity of a color of a line or shape as it is drawn on screen using a pointer, other than a mouse.

For hardware that does not support pressure, including but not limited to mouse, the value must be 1 when in the active buttons state and 0 otherwise.

## Notes

Starting with Internet Explorer 11, this property returns a value of 0.5 for active contact (such as mouse button push) and 0 otherwise on hardware that does not support pressure.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pressure Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772360(v=vs.85).aspx) Article]

