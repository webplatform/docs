---
title: appVersion
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.appVersion](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appVersion) Article]'
  - 'Microsoft Developer Network: [[navigator.appVersion](http://msdn.microsoft.com/en-us/library/ie/ms533080(v=vs.85).aspx) Article]'
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
summary: 'Returns the version of the browser as a string. It may be either a plain version number, like &quot;5.0&quot;, or a version number followed by more detailed information. The HTML5 specification also allows any browser to return &quot;4.0&quot; here, for compatibility reasons.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/appVersion

---
## Summary

Returns the version of the browser as a string. It may be either a plain version number, like &quot;5.0&quot;, or a version number followed by more detailed information. The HTML5 specification also allows any browser to return &quot;4.0&quot; here, for compatibility reasons.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.appVersion;
```

## Return Value

Returns an object of type StringString

The **appVersion** property returns a value based on the application name, application version, and platform. This syntax shows the format of the returned value.

    clientVersion (platform; information; extra Information)
    or
    5.0 (compatible; MSIE 5.5; Windows 98; Win 9x 4.90)

## Examples

This example enumerates the properties of the navigator object for the current web browser and displays them on the screen.

``` js

```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Do not rely on this property to return the correct browser version. In Gecko-based browsers (like Firefox) and WebKit-based browsers (like Chrome and Safari) the returned value starts with "5.0" followed by platform information. In Opera 10 and newer the returned version does not match the actual browser version, either.

## Notes

### Remarks

### Syntax
