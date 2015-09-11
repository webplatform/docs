---
title: pressure
attributions:
  - 'Microsoft Developer Network: [[pressure Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772360(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
  return:
    predicate: 'Returns an object of type '
    value: double
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/pressure

---
## <span>Summary</span>

The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var pressure = event.pressure;
```

## <span>Return Value</span>

Returns an object of type doubledouble

Pressure of the pointer contact in range of 0 to 1.

## <span>Examples</span>

The following is an example of a pointermove event handler that outputs the value of the event.pressure property to a text field in a form (frmOutput);

``` js
function getPressure(evt){
var theform=document.forms.frmOutput;
theform.txtPressure.value=evt.pressure;
}
```

## <span>Usage</span>

     Could be used for example to control the hue or opacity of a color of a line or shape as it is drawn on screen using a pointer, other than a mouse.

For hardware that does not support pressure, including but not limited to mouse, the value must be 1 when in the active buttons state and 0 otherwise.

## <span>Notes</span>

Starting with Internet Explorer 11, this property returns a value of 0.5 for active contact (such as mouse button push) and 0 otherwise on hardware that does not support pressure.

