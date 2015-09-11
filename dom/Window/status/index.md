---
title: status
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[status](https://developer.mozilla.org/en-US/docs/Web/API/Window.status) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Window
summary: 'Sets the text in the status bar at the bottom of the browser or returns the previously set text.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/status

---
## <span>Summary</span>

Sets the text in the status bar at the bottom of the browser or returns the previously set text.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
var message = window.status;
window.status = value;
```

## <span>Return Value</span>

Returns an object of type StringString

The text contents of the userAgents' Status Bar

## <span>Examples</span>

``` js
window.onload=function(){
window.status='loaded.....';
}
```

## <span>Notes</span>

### <span>Remarks</span>

### <span>Syntax</span>

window.status = string; var value = window.status;