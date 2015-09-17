---
title: 'isDefaultNamespace'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isDefaultNamespace](https://developer.mozilla.org/en-US/docs/Web/API/Node.isDefaultNamespace) Article]'
  - 'Microsoft Developer Network: [[isDefaultNamespace Method](http://msdn.microsoft.com/en-us/library/ie/ff975127(v=vs.85).aspx) Article]'
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
standardization_status: 'W3C Recommendation'
summary: 'Indicates whether or not a namespace is the default namespace for a document.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Node/isDefaultNamespace

---
## Summary

Indicates whether or not a namespace is the default namespace for a document.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var isDefault = node.isDefaultNamespace(/* see parameter list */);
```

## Parameters

### namespace

 Data-type
:   String

 The namespace to be compared to the default namespace.

## Return Value

Returns an object of type BooleanBoolean

Whether the namespace specified in the *namespace* parameter is the default namespace for the document.

## Examples

The following example compares the default Namespace of the body element to the SVG namespace and then to the xHTML namespace. false then true is displayed.

``` html
<!DOCTYPE html>
<html>

<head>
<meta content="text/html; charset=utf-8" http-equiv="Content-Type">
<title>isDefaultNamespace example</title>
</head>

<body>


   <script type="text/javascript">//<![CDATA[
    var nsSVG='http://www.w3.org/2000/svg';
    alert(document.body.isDefaultNamespace(nsSVG));
    var nsxHTML='http://www.w3.org/1999/xhtml';
    alert(document.body.isDefaultNamespace(nsxHTML));
   //]]></script>
</body>

</html>
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
