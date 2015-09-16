---
title: 'createNodeIterator'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates a NodeIterator object that you can use to traverse filtered lists of nodes or elements in a document.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createNodeIterator

---
## Summary

Creates a NodeIterator object that you can use to traverse filtered lists of nodes or elements in a document.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var nodeIterator = document.createNodeIterator(rootNode, whatToShow, filter, expandEntityReference);
```

## Parameters

### rootNode

 Data-type
:   DOM Node

 The root element or node to start traversing on.

### whatToShow

 Data-type
:   unsigned long

 The type of nodes or elements to appear in the node list. For more information, see [**whatToShow**](/dom/NodeIterator/whatToShow).

### filter

 Data-type
:   DOM Node

 A custom NodeFilter function to use. For more information, see [**filter**](/dom/NodeIterator/filter). Use null for no filter.

### expandEntityReference

 Data-type
:   Boolean

 Whether entity reference nodes are expanded. For more information, see [**expandEntityReferences**](/dom/NodeIterator/expandEntityReferences).

## Return Value

Returns an object of type DOM NodeDOM Node

A [**NodeIterator**](/dom/NodeIterator) instance object.

## Examples

The following code example shows how to use [**NodeIterator**](/dom/NodeIterator) objects to find and remove references. The iterator returns all text nodes from the document **body** and searches for `Monday` in text and [**id**](/html/attributes/id) attributes of parent nodes. The script matches text by using the [**wholeText**](/dom/Text/wholeText) object of the node.

``` html
<!DOCTYPE html>
<html>
 <head>
  <script>
function noMondays()
{
    var ni = document.createNodeIterator(document.body, NodeFilter.SHOW_TEXT, null, false);

    var textNode = ni.nextNode();
    while (textNode) {
        if (textNode.wholeText.match('Monday') ||
            textNode.parentNode.getAttribute('id') == 'Monday')
        {
            textNode.parentNode.removeChild(textNode);
        }
        textNode = ni.nextNode();
    }
}
function refresh()
{
    window.location.reload( false );    // Reload our page.
}
  </script>
 </head>
 <body>
    <p>Monday, Joe bought a turkey.</p>
    <p>Tuesday, Bill bought a pound of nails.</p>
    <div>Chuck called in sick Monday.</div>
    <p id="Monday">CALL supplier today!</p>
    <p>Wednesday's delivery was delayed.</p>
    <button onclick="refresh()">Reload</button>
    <button onclick="noMondays()">Lose Mondays</button>
 </body>
</html>
```

## Notes

Use the **createNodeIterator** method when you want to focus on node content because [**NodeIterator**](/dom/NodeIterator) traverses a flat list of nodes in the document structure.

## Related specifications

[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/traversal.html#Traversal-Document)
:   Recommendation
