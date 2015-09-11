---
title: clearImmediate
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[clearImmediate](https://developer.mozilla.org/en-US/docs/Web/API/Window.clearImmediate) Article]'
  - 'Microsoft Developer Network: [[clearImmediate Method](http://msdn.microsoft.com/en-us/library/windows/apps/hh965354.aspx) Article]'
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces.'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Cancels a function request created with setImmediate.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/clearImmediate

---
## <span>Summary</span>

Cancels a function request created with setImmediate.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
 window.clearImmediate(/* see parameter list */);
```

## <span>Parameters</span>

### <span>handle</span>

 Data-type
:   Number

 A handle to an immediate callback request, which is the value returned by [**setImmediate**](/dom/Window/setImmediate).

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
var immediateID = setImmediate(function () {
  // Run some code
}

document.getElementById("button").addEventListener('click',function () {
  clearImmediate(immediateID);
}, false);
```

## <span>Notes</span>

### <span>Remarks</span>

### <span>Syntax</span>

### <span>Standards information</span>

-   [Efficient Script Yielding](http://go.microsoft.com/fwlink/p/?linkid=247522)
