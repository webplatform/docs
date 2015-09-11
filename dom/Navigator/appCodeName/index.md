---
title: appCodeName
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.appCodeName](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appCodeName) Article]'
  - 'Microsoft Developer Network: [[navigator.appCodeName](http://msdn.microsoft.com/en-us/library/ie/ms533077(v=vs.85).aspx) Article]'
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
summary: 'Returns the internal &quot;code&quot; name of the current browser. Do not rely on this property to return the correct value.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/appCodeName

---
## <span>Summary</span>

Returns the internal &quot;code&quot; name of the current browser. Do not rely on this property to return the correct value.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = navigator.appCodeName;
```

## <span>Return Value</span>

Returns an object of type StringString

the internal "code" name of the current web browser.

## <span>Examples</span>

the linked example enumerates the navigator object, displaying each property and method on the screen.

``` js
navigator.appCodeName
```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## <span>Usage</span>

     Should not be used to detect the current web browser vendor or "code" name.

### <span>Syntax</span>