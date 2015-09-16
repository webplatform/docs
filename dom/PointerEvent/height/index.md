---
title: height
attributions:
  - 'Microsoft Developer Network: [[height Property - PointerEvent](http://msdn.microsoft.com/en-us/library/ie/dn255064(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'The height (magnitude on the Y axis), in CSS pixels, of the contact geometry of the pointer.'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/height

---
## Summary

The height (magnitude on the Y axis), in CSS pixels, of the contact geometry of the pointer.

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = event.height;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

Resizing an element to match the contact geometry

``` js
<div style="position:absolute; top:0px; left:0px; width:100px;height:100px;"></div>
<script>
window.addEventListener("pointerdown", checkPointerSize, false);
function checkPointerSize(event) {
    event.target.style.width = event.width + "px";
    event.target.style.height = event.height + "px";
}
</script>
```

## Usage

     This value may be updated on each event for a given pointer. For devices which have a contact geometry but the actual geometry is not reported by the hardware, a default value may be provided by the user agent to approximate the geometry typical of that pointer type. Otherwise, the value must be 0.

## Notes

For touch hardware that doesn't support width or height, a CSS document pixel equivalent of 7 millimeters is returned. For mouse or pen input, a value off 1 pixel is returned.

In Internet Explorer 10, the returned value is in screen pixels. In Internet Explorer 11, the returned value is in CSS document pixels, where for example, a div sized to the values of PointerEvent.width and PointerEvent.height would have the same size as the finger contact.

