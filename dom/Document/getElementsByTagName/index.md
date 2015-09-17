---
title: 'getElementsByTagName'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat'
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
summary: 'Returns an HTMLCollection of all descendant elements with a given tag name.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/getElementsByTagName

---
## Summary

Returns an HTMLCollection of all descendant elements with a given tag name.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var object = object.getElementsByTagName(/* see parameter list */);
```

## Parameters

### name

 Data-type
:   String

 The name of an element tag.

## Return Value

Returns an object of type DOM NodeDOM Node

A DOM collection of elements with the given tag name.

## Examples

The following example returns the number of `li` elements (10) and the text of the first one ("Item 1").

``` html
<!doctype html>
<html>
 <head>
  <script>
function printFirstLIText(){
  var aReturn = document.getElementsByTagName("LI");
  alert("Length: " + aReturn.length + "\nFirst Item: " + aReturn[0].childNodes[0].nodeValue);
}
  </script>
 </head>
 <body>

  <ul onclick="printFirstLIText()">
   <li>Item 1
    <ul>
     <li>Sub Item 1.1
      <ol>
       <li>Super Sub Item 1.1</li>
       <li>Super Sub Item 1.2</li>
      </ol>
     </li>
     <li>Sub Item 1.2</li>
     <li>Sub Item 1.3</li>
    </ul>
   </li>
   <li>Item 2
    <ul>
     <li>Sub Item 2.1
     <li>Sub Item 2.3
    </ul>
   </li>
   <li>Item 3</li>
  </ul>

 </body>
</html>
```

## Usage

     Use this method to get a collection of all child and nested child elements with the specified tag name.

## Related specifications

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation
