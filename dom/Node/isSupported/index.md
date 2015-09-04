---
title: isSupported
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Deprecated
summary: 'Returns a value indicating whether or not the object supports a specific DOM standard.'
uri: dom/Node/isSupported

---
# isSupported

## Summary

Returns a value indicating whether or not the object supports a specific DOM standard.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var isSupported = node.isSupported(/* see parameter list */);
```

## Parameters

### feature

 Data-typeÂ
:   String

 The name of the standard.

### version

 Data-typeÂ
:   String

 The version number of the standard. Supported values vary according to the standard.

## Return Value

Returns an object of type Boolean.

Whether the standard is supported.

## Examples

    <div id="divMain">
    </div>

    <script>
     // check to see if its supports the DOM2 HTML Module.
     var main = document.getElementById('divMain');
     var output = main.isSupported('HTML', '2.0');
    </script>

## Notes

Gecko-specific notes

[1] Starting with Gecko 19.0 (Firefox 19.0 / Thunderbird 19.0 / SeaMonkey 2.16) this method will always return true (bug 801425) and starting with Gecko 22.0 (Firefox 22.0 / Thunderbird 22.0 / SeaMonkey 2.19) this method has been removed.

Deprecated This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
[Living Standard](http://dom.spec.whatwg.org/#interface-node)
:   Recommendation

## See also

### External resources

[W3C DOM Conformance Tests](http://www.w3.org/DOM/Test/)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isSupported](https://developer.mozilla.org/en-US/docs/Web/API/Node.isSupported) Article]

Portions of this content come from the Microsoft Developer Network: [[isSupported Method](http://msdn.microsoft.com/en-us/library/ie/ff975130(v=vs.85).aspx) Article]

