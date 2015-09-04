---
title: getNamedItem
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets an attribute with a given name from an element.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getNamedItemEx1.htm'
uri: dom/NamedNodeMap/getNamedItem

---
# getNamedItem

## Summary

Gets an attribute with a given name from an element.

*Method of [dom/NamedNodeMap](/dom/NamedNodeMap)*

## Syntax

``` {.js}
var attribute = attributes.getNamedItem(/* see parameter list */);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the [**attribute**](/dom/HTMLElement) to get.

## Return Value

Returns an object of type DOM Node.

The attribute node with the given name.

## Examples

The following example shows how to use the **getNamedItem** method to retrieve the value of an [**attribute**](/dom/HTMLElement).

``` {.html}
<!doctype html>
<html>
<head>
<title>getNamedItem Example</title>
<script>
function Init()
{
    var oAttrColl = document.getElementById("oElem").attributes;
    var oAttr = oAttrColl.getNamedItem("align");
    console.log("ALIGN attribute value: " + oAttr.value);
}
  </script>
 </head>
 <body onload="Init()">
  <p id="oElem" align="center">An element.</P>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getNamedItemEx1.htm)

## Notes

If the **attribute** applies to an element but is not specified, this method returns the **attribute** with the specified name set to an empty string. If the **attribute** does not apply to the element and is not specified, then an error is returned. If the **attribute** does not apply to the element and is specified, then the **attribute** with the specified name is returned.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[getNamedItem](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]

Portions of this content come from the Microsoft Developer Network: [[getNamedItem Method](http://msdn.microsoft.com/en-us/library/ie/ms536441(v=vs.85).aspx) Article]

