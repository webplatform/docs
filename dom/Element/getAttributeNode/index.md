---
title: getAttributeNode
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Retrieves an attribute node by name.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/getAttributeNode

---
## Summary

Retrieves an attribute node by name.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var attributeNode = element.getAttributeNode();
```

## Return Value

Returns an object of type DOM NodeDOM Node

An attribute node.

## Examples

The following example uses **getAttributeNode** to create an attribute and populate its **div** element. Note how the call to [**setAttribute**](/dom/Element/setAttribute) changes the [**href**](/html/attributes/href) value for the content attribute but not for the DOM attribute.

``` html
<!doctype html>
<html>
 <head>
  <title>Attribute Node Example</title>
  <base href="http://msdn.microsoft.com/">
  <script>
function GetAttrNode() {
  //Retrieve an attribute node and a DOM attribute.
  var o = document.getElementById("msdn");
  var sDomAttr = o.href;

  o.setAttribute('href', 'en-us/ie/default.aspx');
  var sContentAttr = o.getAttributeNode("href");
  var sOutput = ("Content attribute node value: " + sContentAttr.value +
              "<br/>DOM attribute value: " + sDomAttr);

  document.getElementById("output").innerHTML = sOutput;
}
  </script>
 </head>
 <body>
   <a id="msdn" href="en-us/default.aspx">Microsoft Developer Network</a>
   <div id="output" onmouseover="GetAttrNode()">Point here to display attribute values.</div>
 </body>
</html>
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
