---
title: defaultStatus
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Mixed
summary: 'Sets or retrieves the default message displayed in the status bar at the bottom of the window. '
uri: dom/Window/defaultStatus

---
# defaultStatus

## Summary

Sets or retrieves the default message displayed in the status bar at the bottom of the window.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var statusMessage = window.defaultStatus;
window.defaultStatus = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The default message to display on the userAgents' Status Bar.

## Examples

The following example displays 'Welcome to our website' in the userAgent's Status Bar when the page loads.

``` {.js}
window.onload=function(){
window.defaultStatus='Welcome to our website!';

};
```

## Usage

     Use to customize the userAgent default Status Bar message.

## Notes

### Remarks

Do not confuse **defaultStatus** with [**status**](/dom/Window/status). The **status** property reflects a priority or transient message in the status bar, such as the message that appears when an [**onmouseover**](/dom/MouseEvent/mouseover) event occurs over an anchor. Windows Internet Explorer 7: References to this property are ignored if the "Allow status bar updates via script" option is disabled or the URLACTION \_FEATURE\_SCRIPT\_STATUS\_BAR URL action is disallowed for the current URL security zone. For more information on URL security zones, please see About URL Security Zones.

#### defaultStatus in Metro style apps using JavaScript

Metro style apps using JavaScript don't support this property because they don't have status bars.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[defaultStatus](https://developer.mozilla.org/en-US/docs/Web/API/Window.defaultStatus) Article]

Portions of this content come from the Microsoft Developer Network: [[defaultStatus Property](http://msdn.microsoft.com/en-us/library/ie/ms533717(v=vs.85).aspx) Article]

