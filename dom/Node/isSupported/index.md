---
title: isSupported
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isSupported](https://developer.mozilla.org/en-US/docs/Web/API/Node.isSupported) Article]'
  - 'Microsoft Developer Network: [[isSupported Method](http://msdn.microsoft.com/en-us/library/ie/ff975130(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Node
standardization_status: Deprecated
summary: 'Returns a value indicating whether or not the object supports a specific DOM standard.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/isSupported

---
## Summary

Returns a value indicating whether or not the object supports a specific DOM standard.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var isSupported = node.isSupported(/* see parameter list */);
```

## Parameters

### feature

 Data-type
:   String

 The name of the standard.

### version

 Data-type
:   String

 The version number of the standard. Supported values vary according to the standard.

## Return Value

Returns an object of type BooleanBoolean

Whether the standard is supported.

## Examples

``` html
<div id="divMain">
</div>

<script>
 // check to see if its supports the DOM2 HTML Module.
 var main = document.getElementById('divMain');
 var output = main.isSupported('HTML', '2.0');
</script>
```

## Notes

Gecko-specific notes

[1] Starting with Gecko 19.0 (Firefox 19.0 / Thunderbird 19.0 / SeaMonkey 2.16) this method will always return true (bug 801425) and starting with Gecko 22.0 (Firefox 22.0 / Thunderbird 22.0 / SeaMonkey 2.19) this method has been removed.

Deprecated This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Living Standard](http://dom.spec.whatwg.org/#interface-node)
:   Recommendation

## See also

### External resources

[W3C DOM Conformance Tests](http://www.w3.org/DOM/Test/)
