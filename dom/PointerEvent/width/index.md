---
title: width
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The width (magnitude on the X axis), in CSS pixels, of the contact geometry of the pointer.'
uri: dom/PointerEvent/width

---
# width

## Summary

The width (magnitude on the X axis), in CSS pixels, of the contact geometry of the pointer.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PointerEvent](/dom/PointerEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = event.width;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

Resizing an element to match the contact geometry

``` {.js}

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[width Property PointerEvent](http://msdn.microsoft.com/en-us/library/ie/dn255065(v=vs.85).aspx) Article]

