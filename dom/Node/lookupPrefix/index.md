---
title: lookupPrefix
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.lookupPrefix](https://developer.mozilla.org/en-US/docs/Web/API/Node.lookupPrefix) Article]'
  - 'Microsoft Developer Network: [[lookupPrefix Method](http://msdn.microsoft.com/en-us/library/ie/ff975159(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Gets the namespace prefix associated with a URI, if any.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/lookupPrefix

---
## Summary

Gets the namespace prefix associated with a URI, if any.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var prefix = node.lookupPrefix(/* see parameter list */);
```

## Parameters

### namespaceURI

 Data-type
:   String

 The namespace URI.

## Return Value

Returns an object of type StringString

The namespace prefix associated with the URI, or null if none is found.

## Examples

``` html
<html xmlns="http://www.w3.org/1999/xhtml"  xmlns:svg="http://www.w3.org/2000/svg">
   <script type="text/javascript">//<![CDATA[
    var nsxml = 'http://www.w3.org/1999/xhtml';
    var nssvg = 'http://www.w3.org/2000/svg';
    alert('root element nsprefix is ' + document.documentElement.lookupPrefix(nssvg));
   //]]></script>
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
