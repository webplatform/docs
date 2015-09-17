---
title: 'getElementsByClassName'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs mobile compat'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /dom/Document
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets a collection of all descendant elements with given classes. Not recommended; see Notes.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/getElementsByClassName

---
## Summary

Gets a collection of all descendant elements with given classes. Not recommended; see Notes.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var elements = document.getElementsByClassName(classNames);
```

## Parameters

### classNames

 Data-type
:   String

 A space separated list of classes.

## Return Value

Returns an object of type ObjectObject

A live [HTMLCollection](/dom/HTMLCollection) of elements with the given class names.

## Examples

This example returns the number of `li` tags whose class is "sublistitem" (3), and the text of the first one ("Sub Item 1.1").

``` html
<!doctype html>
<html>
 <head>
  <script>
function printFirstSubLIText(){
  var aReturn = document.getElementsByClassName("sublistitem");
  alert("Length: " + aReturn.length + "\nFirst Item: " + aReturn[0].childNodes[0].nodeValue);
}
  </script>
 </head>

 <body>
  <ul onclick="printFirstSubLIText()">
   <li>Item 1
    <ul>
     <li class="sublistitem">Sub Item 1.1
      <ol>
       <li>Super Sub Item 1.1</li>
       <li>Super Sub Item 1.2</li>
      </ol>
     </li>
     <li class="sublistitem">Sub Item 1.2</li>
     <li class="sublistitem">Sub Item 1.3</li>
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

     The use of this property is discouraged. See the Notes section for details.

## Notes

The use of this property is discouraged because of performance implications (due to the live DOMCollection where any changes to the document must be reflected on the returned object immediately) and complexity (the removal of an element from the document will result in immediate changes to the collection).

A close alternative is

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Candidate Recommendation
