---
title: getElementById
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
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
summary: 'Gets an element with a specified ID.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/getElementById

---
## Summary

Gets an element with a specified ID.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var element = document.getElementById(id);
```

## Parameters

### id

 Data-type
:   String

 The ID to match.

## Return Value

Returns an object of type DOM NodeDOM Node

An element that matches the specified ID. If there are multiple matches, the first is returned. If there is no match, `null` is returned.

## Examples

The following example uses **getElementById** to display the content of the first **div** element in a collection with the [**ID**](/html/attributes/id) attribute value, `div1`, when a button is clicked.

``` html
&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;"Show First DIV Content"&lt;/title&gt;
  &lt;meta charset="utf-8"/&gt;
  &lt;script type="text/javascript"&gt;
function getID() {
   // Display the content of the first DIV element in the collection.
   var div = document.getElementById("div1");
   alert("The content of the first DIV element is " + "\"" + div.innerHTML + "\".");
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;div id="div1"&gt;Div #1&lt;/div&gt;
  &lt;div id="div2"&gt;Div #2&lt;/div&gt;
  &lt;div id="div3"&gt;Div #3&lt;/div&gt;
  &lt;input type="button" value="Show First DIV Content" onclick="getID()"&gt;
 &lt;/body&gt;
&lt;/html&gt;
```

## Related specifications

[DOM Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/core.html#ID-getElBId)
:   Recommendation

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-getElBId)
:   Recommendation

[W3C DOM4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-nonelementparentnode-getelementbyid)
:   Candidate Recommendation

**Deletion Candidate**: This page is a candidate for deletion

