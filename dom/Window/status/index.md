---
title: status
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Sets the text in the status bar at the bottom of the browser or returns the previously set text.'
uri: dom/Window/status

---
# status

## Summary

Sets the text in the status bar at the bottom of the browser or returns the previously set text.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var message = window.status;
window.status = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text contents of the userAgents' Status Bar

## Examples

``` {.js}
window.onload=function(){
window.status='loaded.....';
}
```

## Notes

### Remarks

### Syntax

window.status = string; var value = window.status;

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[status](https://developer.mozilla.org/en-US/docs/Web/API/Window.status) Article]

