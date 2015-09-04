---
title: index
tags:
  0: API
  1: Object
  2: Properties
  4: Gamepad
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The index of the gamepad in the Navigator.'
uri: apis/gamepad/Gamepad/index

---
# index

## Summary

The index of the gamepad in the Navigator.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/gamepad/Gamepad](/apis/gamepad/Gamepad)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.index;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

The Gamepad API provides a function, [Navigator.getGamepads](/dom/Navigator/getGamepads), that returns a list of all devices currently visible to the web page, as an array of Gamepad objects. When a gamepad is connected, this example reports its index, id, number of buttons, number of axes, and when the gamepad data was updated.

``` {.js}
window.addEventListener("gamepadconnected", function(e) {
  var gp = navigator.getGamepads()[e.gamepad.index];
  console.log("Gamepad connected.");
  console.log("Gamepad index:", gp.index);
  console.log("Gamepad id:", gp.id);
  console.log("Gamepad buttons:", gp.buttons.length);
  console.log("Gamepad axes:", gp.axes.length);
  console.log("Gamepad last updated:", gp.timestamp);
});
```

## Related specifications

Specification
:   Status
[W3C Gamepad Specification](https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/Guide/API/Gamepad)

