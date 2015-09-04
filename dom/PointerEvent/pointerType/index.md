---
title: pointerType
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Indicates the device type that caused the event (mouse, pen, touch, etc.).'
uri: dom/PointerEvent/pointerType

---
# pointerType

## Summary

Indicates the device type that caused the event (mouse, pen, touch, etc.).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = event.pointerType;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

Detecting the type of input from a user

``` {.js}
window.addEventListener("pointerdown", detectInputType, false);
function detectInputType(event) {
    switch(event.pointerType) {
        case "mouse":
            alert("You used a mouse!");
            break;
        case "pen":
            alert("You used a pen stylus!");
            break;
        case "touch":
            alert("You used touch!");
            break;
        default:
            alert("Not sure what device was used!");
    }
}
```

## Usage

     If a user agent is to fire a pointer event for a mouse, pen stylus, or touch input device, then the value of pointerType must be according to the following table:

Pointer Device Type
:   pointerType Value
Mouse
:   mouse
Pen Stylus
:   pen
Touch Contact
:   touch

If the device type cannot be detected by the user agent, then the value must be an empty string. If a user agent supports pointer device types other than those listed above, the value of pointerType should be vendor prefixed to avoid conflicting names for different types of devices. Future specifications may provide additional normative values for other device types.

## Notes

In Internet Explorer 11, this property has been changed to return a string value. In Internet Explorer 10, it provided a return type of long: •MSPOINTER\_TYPE\_TOUCH: 0x00000002 •MSPOINTER\_TYPE\_PEN: 0x00000003 •MSPOINTER\_TYPE\_MOUSE: 0x00000004

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointerType Property](http://msdn.microsoft.com/en-us/library/ie/hh772359(v=vs.85).aspx) Article]

