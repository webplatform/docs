---
title: 'platform'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.platform](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.platform) Article]'
  - 'Microsoft Developer Network: [[navigator.platform](http://msdn.microsoft.com/en-us/library/ie/ms534340(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/b0053b13f0dc7d3b8e0c/e7a999df33666b9d624c77ef0d824ad90023842a'
notes:
  - 'Return values for Android, iOS and blackberry operating systems from browsers hosted on non-wintel OS.'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: "Retrieves the name of the user's operating system.\n"
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/platform

---
## Summary

Retrieves the name of the user's operating system.

In IE10 and higher and WaterFox browsers this will return the bitness of the current tab. eg

Win32 or Win64.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var returnValue = navigator.platform;
```

## Return Value

Returns an object of type StringString

HP-UX

HP UNIX-based computers.

MacPPC

Macintosh PowerPC-based computers.

Mac68K

Macintosh 68K-based computers.

SunOS

Solaris-based computers.

Win64

Windows 64-bit platform.

Win32

Windows 32-bit platform.

Win16

Windows 16-bit platform.

WinCE

Windows CE platform.

## Examples

The external example enums the properties and methods of the navigator object of the client web browser and displays the results on the screen.

``` html

```

[View live example](http://result.dabblet.com/gist/b0053b13f0dc7d3b8e0c/e7a999df33666b9d624c77ef0d824ad90023842a)

## Usage

     Could be used to feature test for support for x86 plugins or ActiveX controls.

To determine what bitness a web page is being rendered with, and subsequently the required bitness of any ActiveX controls it may be hosting type javascript:alert(navigator.platform); in the browser's Address bar.

### Syntax

var platform = navigator.platform

## Related specifications

[DOM Navigator Platform](http://www.w3.org/TR/html5/webappapis.html#dom-navigator-platform)
:   Draft
