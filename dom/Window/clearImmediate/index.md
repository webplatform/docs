---
title: clearImmediate
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces.'
summary: 'Cancels a function request created with setImmediate.'
uri: dom/Window/clearImmediate

---
# clearImmediate

## Summary

Cancels a function request created with setImmediate.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 window.clearImmediate(/* see parameter list */);
```

## Parameters

### handle

 Data-typeÂ
:   Number

 A handle to an immediate callback request, which is the value returned by [**setImmediate**](/dom/Window/setImmediate).

## Return Value

No return value

## Examples

``` {.js}
var immediateID = setImmediate(function () {
  // Run some code
}

document.getElementById("button").addEventListener('click',function () {
  clearImmediate(immediateID);
}, false);
```

## Notes

### Remarks

### Syntax

### Standards information

-   [Efficient Script Yielding](http://go.microsoft.com/fwlink/p/?linkid=247522)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[clearImmediate](https://developer.mozilla.org/en-US/docs/Web/API/Window.clearImmediate) Article]

Portions of this content come from the Microsoft Developer Network: [[clearImmediate Method](http://msdn.microsoft.com/en-us/library/windows/apps/hh965354.aspx) Article]

