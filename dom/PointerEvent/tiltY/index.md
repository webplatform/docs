---
title: 'tiltY'
attributions:
  - 'Microsoft Developer Network: [[tiltY Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772365(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'The plane angle (in degrees, in the range of [-90,90]) between the X-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the X axis.'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/tiltY

---
## Summary

The plane angle (in degrees, in the range of [-90,90]) between the X-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the X axis.

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = event.tiltY;
```

## Return Value

Returns an object of type NumberNumber

A value between -90 and +90

## Examples

The following is an example of a pointer event handler that outputs the value of the tiltX property to a text field, txtTiltY.

``` js
function getTiltY(evt){
var theform=document.forms.frmOutput;
theform.txtTiltY.value=evt.tiltY;
}
```

## Usage

     A positive tiltY is towards the user. tiltY can be used along with tiltX to represent the tilt away from the normal of a transducer with the digitzer. For devices that do not report tilt, the value must be 0.

![caption](/assets/public/6/62/TiltY.png)

