---
title: lookupPrefix
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'needs example'
summary: 'Gets the namespace prefix associated with a URI, if any.'
uri: dom/Node/lookupPrefix

---
# lookupPrefix

## Summary

Gets the namespace prefix associated with a URI, if any.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var prefix = node.lookupPrefix(/* see parameter list */);
```

## Parameters

### namespaceURI

 Data-typeÂ
:   String

 The namespace URI.

## Return Value

Returns an object of type String.

The namespace prefix associated with the URI, or null if none is found.

## Examples

    <html xmlns="http://www.w3.org/1999/xhtml"  xmlns:svg="http://www.w3.org/2000/svg">
       <script type="text/javascript">//<![CDATA[
        var nsxml = 'http://www.w3.org/1999/xhtml';
        var nssvg = 'http://www.w3.org/2000/svg';
        alert('root element nsprefix is ' + document.documentElement.lookupPrefix(nssvg));
       //]]></script>

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.lookupPrefix](https://developer.mozilla.org/en-US/docs/Web/API/Node.lookupPrefix) Article]

Portions of this content come from the Microsoft Developer Network: [[lookupPrefix Method](http://msdn.microsoft.com/en-us/library/ie/ff975159(v=vs.85).aspx) Article]

