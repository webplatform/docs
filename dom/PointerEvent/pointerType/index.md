---
title: 'pointerType'
attributions:
  - 'Microsoft Developer Network: [[pointerType Property](http://msdn.microsoft.com/en-us/library/ie/hh772359(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'Indicates the device type that caused the event (mouse, pen, touch, etc.).'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/pointerType

---
## Summary

Indicates the device type that caused the event (mouse, pen, touch, etc.).

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = event.pointerType;
```

## Return Value

Returns an object of type StringString

## Examples

Detecting the type of input from a user

``` js
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

|Pointer Device Type|pointerType Value|
|:------------------|:----------------|
|Mouse|mouse|
|Pen Stylus|pen|
|Touch Contact|touch|

If the device type cannot be detected by the user agent, then the value must be an empty string. If a user agent supports pointer device types other than those listed above, the value of pointerType should be vendor prefixed to avoid conflicting names for different types of devices. Future specifications may provide additional normative values for other device types.

## Notes

In Internet Explorer 11, this property has been changed to return a string value. In Internet Explorer 10, it provided a return type of long: •MSPOINTER\_TYPE\_TOUCH: 0x00000002 •MSPOINTER\_TYPE\_PEN: 0x00000003 •MSPOINTER\_TYPE\_MOUSE: 0x00000004

