---
title: getAttributeNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat'
summary: 'Retrieves an attribute node by name.'
uri: dom/Element/getAttributeNode

---
# getAttributeNode

## Summary

Retrieves an attribute node by name.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var attributeNode = element.getAttributeNode();
```

## Return Value

Returns an object of type DOM Node.

An attribute node.

## Examples

The following example uses **getAttributeNode** to create an attribute and populate its **div** element. Note how the call to [**setAttribute**](/dom/Element/setAttribute) changes the [**href**](/html/attributes/href) value for the content attribute but not for the DOM attribute.

``` {.html}
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

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

