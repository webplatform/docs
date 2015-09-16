---
title: 'setNamedItem'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
  - 'Microsoft Developer Network: [[setNamedItem Method](http://msdn.microsoft.com/en-us/library/ie/ms536751(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setNamedItemEx1.htm'
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
standardization_status: 'W3C Recommendation'
summary: 'Adds an attribute to an element by using an attributes collection.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/NamedNodeMap/setNamedItem

---
## Summary

Adds an attribute to an element by using an attributes collection.

Method of [dom/NamedNodeMap](/dom/NamedNodeMap)[dom/NamedNodeMap](/dom/NamedNodeMap)

## Syntax

``` js
var object = object.setNamedItem(/* see parameter list */);
```

## Parameters

### ppNode

 Data-type
:   any

**attribute**

## Return Value

Returns an object of type DOM NodeDOM Node

**IHTMLDOMAttribute**

**attribute**

attribute

## Examples

The following example shows how to add an attribute to an element using the **setNamedItem** method.

``` html
<html>
<head>
<title>setNamedItem example</title>
<script>
function fnSetNamedItem(){
var nnm = myDIV.attributes;
var namedItem = document.createAttribute("title");
namedItem.value = "This is a ToolTip";
nnm.setNamedItem(namedItem);
}
</script>
</head>
<body onload="fnSetNamedItem();">
<div id="myDIV">This DIV now has a ToolTip.</div>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setNamedItemEx1.htm)

## Notes

### Remarks

An [**attribute**](/dom/HTMLElement) that is set with this method does not have to apply to the element. If an **attribute** with the same name is already present, it is replaced by the new **attribute**. **setNamedItem** was introduced in Microsoft Internet Explorer 6.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4
