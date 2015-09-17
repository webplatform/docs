---
title: 'tiltX'
attributions:
  - 'Microsoft Developer Network: [[tiltX Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772364(v=vs.85).aspx) Article]'
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
summary: 'The plane angle (in degrees, in the range of [-90,90]) between the Y-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the Y axis.'
tags:
  - API_Object_Properties
uri: dom/PointerEvent/tiltX

---
## Summary

The plane angle (in degrees, in the range of [-90,90]) between the Y-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the Y axis.

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = event.tiltX;
```

## Return Value

Returns an object of type NumberNumber

## Examples

The following is an example of a pointer event handler that outputs the value of the tiltX property to a text field, txtTiltX.

``` js
function getTiltX(evt){
var theform=document.forms.frmOutput;
theform.txtTiltX.value=evt.tiltX;
}
```

## Usage

     A positive tiltX is to the right. tiltX can be used along with tiltY to represent the tilt away from the normal of a transducer with the digitizer. For devices that do not report tilt, the value must be 0.

![caption](/assets/public/2/20/TiltX.png)

