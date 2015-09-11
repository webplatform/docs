---
title: lastElementChild
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat and better standards link'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the last child of this node that is an element, if there are any element children, or null otherwise. Read-only.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Element/lastElementChild

---
## <span>Summary</span>

Retrieves the last child of this node that is an element, if there are any element children, or null otherwise. Read-only.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.lastElementChild;
```

## <span>Examples</span>

This example shows how to get the content of a list using firstElementChild, nextElementSibling, previousElementSibling, and lastElementChild to traverse the document tree.

``` html
<!DOCTYPE html>
<html>
<head>
<title>IElementTraversal Example</title>
    <script>
        function GetListItems () {
            var list = document.getElementById ("girls");       // find our list
            var results = document.getElementById("results");   // get our results line element
            var oChild = list.lastElementChild;                 // start with the last item in list
            while (oChild) {                                    // get and display each item in list
               results.innerHTML += "<br/>" + oChild.innerHTML;
                oChild = oChild.previousElementSibling;         // get previous element in list
                }
        }
        function GetListItems2 () {
            var list = document.getElementById ("girls");       // find our list
            var results = document.getElementById("results");   // get our results line element
            var oChild = list.firstElementChild;                // start with the first item in list
            while (oChild) {                                    // get and display each item in list
                results.innerHTML += "<br />" + oChild.innerHTML;
                oChild = oChild.nextElementSibling;             // get next element in list
                }
        }
        function refresh()
           {
             window.location.reload( false );           //reload our page
           }
    </script>
</head>
<body>
    <ol id="girls">
        <li>Sugar</li>
        <li>Spice</li>
        <li>Everything nice</li>
    </ol>
    <p id="results">Girls have: </p>
    <p>
    <button onclick="GetListItems ();">Get list backwards</button>
    </p>
   <p>
    <button onclick="GetListItems2 ();">Get list forwards</button>
    </p>
    <p>
      <input type="button" value="Refresh page" onclick="refresh()"   />
    </p>
</body>
</html>
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [Element Traversal Specification](http://go.microsoft.com/fwlink/p/?linkid=182722), Section 2.2
