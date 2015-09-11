---
title: id
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/Guide/API/Gamepad)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/gamepad/Gamepad
    href: /apis/gamepad/Gamepad
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/gamepad/Gamepad
standardization_status: 'W3C Working Draft'
summary: 'A string that identifies the brand or style of connected gamepad device.'
tags:
  0: API
  1: Object
  2: Properties
  4: Gamepad
uri: apis/gamepad/Gamepad/id

---
## <span>Summary</span>

A string that identifies the brand or style of connected gamepad device.

Property of [apis/gamepad/Gamepad](/apis/gamepad/Gamepad)[apis/gamepad/Gamepad](/apis/gamepad/Gamepad)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = object.id;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

The Gamepad API provides a function, [Navigator.getGamepads](/dom/Navigator/getGamepads), that returns a list of all devices currently visible to the web page, as an array of Gamepad objects. When a gamepad is connected, this example reports its index, id, number of buttons, number of axes, and when the gamepad data was updated.

``` js
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

## <span>Related specifications</span>

[W3C Gamepad Specification](https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html)
:   W3C Working Draft
