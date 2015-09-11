---
title: defaultStatus
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[defaultStatus](https://developer.mozilla.org/en-US/docs/Web/API/Window.defaultStatus) Article]'
  - 'Microsoft Developer Network: [[defaultStatus Property](http://msdn.microsoft.com/en-us/library/ie/ms533717(v=vs.85).aspx) Article]'
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
standardization_status: Mixed
summary: 'Sets or retrieves the default message displayed in the status bar at the bottom of the window. '
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/defaultStatus

---
## <span>Summary</span>

Sets or retrieves the default message displayed in the status bar at the bottom of the window.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
var statusMessage = window.defaultStatus;
window.defaultStatus = value;
```

## <span>Return Value</span>

Returns an object of type StringString

The default message to display on the userAgents' Status Bar.

## <span>Examples</span>

The following example displays 'Welcome to our website' in the userAgent's Status Bar when the page loads.

``` js
window.onload=function(){
window.defaultStatus='Welcome to our website!';

};
```

## <span>Usage</span>

     Use to customize the userAgent default Status Bar message.

## <span>Notes</span>

### <span>Remarks</span>

Do not confuse **defaultStatus** with [**status**](/dom/Window/status). The **status** property reflects a priority or transient message in the status bar, such as the message that appears when an [**onmouseover**](/dom/MouseEvent/mouseover) event occurs over an anchor. Windows Internet Explorer 7: References to this property are ignored if the "Allow status bar updates via script" option is disabled or the URLACTION \_FEATURE\_SCRIPT\_STATUS\_BAR URL action is disallowed for the current URL security zone. For more information on URL security zones, please see About URL Security Zones.

#### <span>defaultStatus in Metro style apps using JavaScript</span>

Metro style apps using JavaScript don't support this property because they don't have status bars.

### <span>Syntax</span>