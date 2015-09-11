---
title: removeNamedItem
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm'
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
summary: 'Removes an attribute with a given name.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/NamedNodeMap/removeNamedItem

---
## <span>Summary</span>

Removes an attribute with a given name.

Method of [dom/NamedNodeMap](/dom/NamedNodeMap)[dom/NamedNodeMap](/dom/NamedNodeMap)

## <span>Syntax</span>

``` js
var attribute = attributes.removeNamedItem(/* see parameter list */);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   String

 The name of an [**attribute**](/dom/HTMLElement) to remove.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The removed attribute.

## <span>Examples</span>

The following example shows how to use this method to remove an [**attribute**](/dom/HTMLElement) from an element.

``` html
<!doctype html>
<html>
 <head>
<title>removeNamedItem example</title>
  <script>
function removeAttrib() {
    var attributes = document.getElementById("ex").attributes;
    attributes.removeNamedItem("title");
}
  </script>
 </head>
 <body>
 <!-- Although this is possible, **Please, DON'T!**. Buttons are perfect to be clicked on! -->
 <div onclick="removeAttrib();" id="ex" title="This is a tooltip">
Click this DIV and the tooltip will be deactivated.</div>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm)

## <span>Notes</span>

An **attribute** that is removed with this method reverts to the default value of the **attribute** when applicable. This method returns a script error if the user attempts to remove a non-existent attribute node. **removeNamedItem** was introduced in Microsoft Internet Explorer 6.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
