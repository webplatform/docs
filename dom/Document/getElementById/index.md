---
title: getElementById
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets an element with a specified ID.'
uri: dom/Document/getElementById

---
# getElementById

## Summary

Gets an element with a specified ID.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var element = document.getElementById(id);
```

## Parameters

### id

 Data-typeÂ
:   String

 The ID to match.

## Return Value

Returns an object of type DOM Node.

An element that matches the specified ID. If there are multiple matches, the first is returned. If there is no match, `null` is returned.

## Examples

The following example uses **getElementById** to display the content of the first **div** element in a collection with the [**ID**](/html/attributes/id) attribute value, `div1`, when a button is clicked.

``` {.html}
<!doctype html>
<html>
 <head>
  <title>"Show First DIV Content"</title>
  <meta charset="utf-8"/>
  <script type="text/javascript">
function getID() {
   // Display the content of the first DIV element in the collection.
   var div = document.getElementById("div1");
   alert("The content of the first DIV element is " + "\"" + div.innerHTML + "\".");
}
  </script>
 </head>
 <body>
  <div id="div1">Div #1</div>
  <div id="div2">Div #2</div>
  <div id="div3">Div #3</div>
  <input type="button" value="Show First DIV Content" onclick="getID()">
 </body>
</html>
```

## Related specifications

Specification
:   Status
[DOM Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/core.html#ID-getElBId)
:   Recommendation
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-getElBId)
:   Recommendation
[W3C DOM4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-nonelementparentnode-getelementbyid)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

**Deletion Candidate**: This page is a candidate for deletion

