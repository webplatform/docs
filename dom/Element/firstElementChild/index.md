---
title: firstElementChild
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs compat and better spec link'
summary: 'Retrieves the first child of this node that is an element, if there is one, or null otherwise.  Read-only.'
uri: dom/Element/firstElementChild

---
# firstElementChild

## Summary

Retrieves the first child of this node that is an element, if there is one, or null otherwise. Read-only.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.firstElementChild;
```

## Examples

This example shows how to get the content of a list using firstElementChild, nextElementSibling, previousElementSibling, and lastElementChild to traverse the document tree.

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

### Syntax

### Standards information

-   [Element Traversal Specification](http://go.microsoft.com/fwlink/p/?linkid=182722), Section 2.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

