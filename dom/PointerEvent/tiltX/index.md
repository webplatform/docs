---
title: tiltX
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The plane angle (in degrees, in the range of [-90,90]) between the Y-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the Y axis.'
uri: dom/PointerEvent/tiltX

---
# tiltX

## Summary

The plane angle (in degrees, in the range of [-90,90]) between the Y-Z plane and the plane containing both the transducer (e.g. pen stylus) axis and the Y axis.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = event.tiltX;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

The following is an example of a pointer event handler that outputs the value of the tiltX property to a text field, txtTiltX.

``` {.js}
function getTiltX(evt){
var theform=document.forms.frmOutput;
theform.txtTiltX.value=evt.tiltX;
}
```

## Usage

     A positive tiltX is to the right. tiltX can be used along with tiltY to represent the tilt away from the normal of a transducer with the digitizer. For devices that do not report tilt, the value must be 0.

![caption](/assets/public/2/20/TiltX.png)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[tiltX Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/hh772364(v=vs.85).aspx) Article]

