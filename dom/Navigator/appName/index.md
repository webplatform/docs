---
title: 'appName'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.appName](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appName) Article]'
  - 'Microsoft Developer Network: [[navigator.appName](http://msdn.microsoft.com/en-us/library/ie/ms533079(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
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
summary: "appName Returns a string with the name of the browser/user agent.\nThe HTML5 specification also allows any browser to return &quot;Netscape&quot; here, for compatibility reasons.\n"
tags:
  - API_Object_Properties
  - DOM
  - JavaScript
uri: dom/Navigator/appName

---
## Summary

appName Returns a string with the name of the browser/user agent. The HTML5 specification also allows any browser to return &quot;Netscape&quot; here, for compatibility reasons.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.appName;
```

## Return Value

Returns an object of type StringString

Microsoft Internet Explorer

Returned by Internet Explorer 10 and earlier.

Netscape

Default. Returned by Netscape Navigator, Google Chrome, Mozilla Firefox, and IE11.

MSAppHost/1.0

Returned by WWAHost.exe.

## Examples

``` js
var browserName = navigator.appName;
//broswerName returns "Netscape"
```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

### Syntax
