---
title: getNamedItemNS
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
  - 'Microsoft Developer Network: [[getNamedItemNS Method](http://msdn.microsoft.com/en-us/library/ie/ff975126(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/NamedNodeMap
    href: /dom/NamedNodeMap
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/NamedNodeMap
summary: 'Gets an attribute with a given name and a given namespace.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/NamedNodeMap/getNamedItemNS

---
## <span>Summary</span>

Gets an attribute with a given name and a given namespace.

Method of [dom/NamedNodeMap](/dom/NamedNodeMap)[dom/NamedNodeMap](/dom/NamedNodeMap)

## <span>Syntax</span>

``` js
var attribute = attributes.getNamedItemNS(/* see parameter list */);
```

## <span>Parameters</span>

### <span>namespace</span>

 Data-type
:   String

 The namespace name of the attribute to get.

### <span>name</span>

 Data-type
:   String

 The local name of the desired attribute within the specified namespace.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The attribute with the name and namespace.

## <span>Examples</span>

Create a SVG circle element.

``` js
var nsSVG='http://www.w3.org/2000/svg';
var osvgCircleTag=document.createElementNS(nsSVG,'circle');
alert(osvgCircleTag.getNamedItemNS(nsSVG,'r');
```

## <span>Usage</span>

     Used to create and manipulate XML and SVG documents.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
