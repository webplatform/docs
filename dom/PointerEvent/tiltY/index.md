---
title: tiltY
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The plane angle (in degrees, in the range of [-90,90]) between the X-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the X axis.'
uri: dom/PointerEvent/tiltY

---
# tiltY

## Summary

The plane angle (in degrees, in the range of [-90,90]) between the X-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the X axis.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = event.tiltY;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

A value between -90 and +90

## Examples

The following is an example of a pointer event handler that outputs the value of the tiltX property to a text field, txtTiltY.

``` {.js}
function getTiltY(evt){
var theform=document.forms.frmOutput;
theform.txtTiltY.value=evt.tiltY;
}
```

## Usage

     A positive tiltY is towards the user. tiltY can be used along with tiltX to represent the tilt away from the normal of a transducer with the digitzer. For devices that do not report tilt, the value must be 0.

![caption](/assets/public/6/62/TiltY.png)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[tiltY Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772365(v=vs.85).aspx) Article]

