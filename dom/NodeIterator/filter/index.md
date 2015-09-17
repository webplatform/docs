---
title: 'filter'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.filter](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.filter) Article]'
  - 'Microsoft Developer Network: [[filter Property](http://msdn.microsoft.com/en-us/library/ie/ff974820(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/NodeIterator
standardization_status: 'W3C Recommendation'
summary: 'Gets the currently applied NodeFilter to the traversal.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/NodeIterator/filter

---
## Summary

Gets the currently applied NodeFilter to the traversal.

Property of [dom/NodeIterator](/dom/NodeIterator)[dom/NodeIterator](/dom/NodeIterator)

## Syntax

**Note**: This property is read-only.

``` js
var nodeFilter = nodeIterator.filter;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The **NodeFilter** that was applied while traversing.

## Examples

The following example searches for [**table**](/html/elements/table) and [**anchor**](/html/elements/a) tags and reports the value of the [**id**](/html/attributes/id) attribute. Although the [**TreeWalker**](/dom/TreeWalker) preserves the hierarchical relationship of nodes, you don't need to write recursive functions to walk the nodes in a hierarchy. The **NodeFilter** function skips nodes rather than rejecting them, which allows the function to examine all child nodes in the hierarchy.

``` html
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript">
// This is the NodeFilter function. It receives a node, and must return a NodeFilter flag.
function filter(node)
{
    if (node.tagName == "TABLE" || node.tagName == "A")
        return NodeFilter.FILTER_ACCEPT;
    return NodeFilter.FILTER_SKIP;
}
function findNodes()
{
    var tw = document.createTreeWalker(document.body, NodeFilter.SHOW_ELEMENT, filter, false);

    var node, results = '';
    while (node = tw.nextNode()) {
        results += node.id + "<br/>";
    }

    document.getElementById("results").innerHTML += results;
}
function refresh()
{
    window.location.reload( false );    // Reload our page.
}
</script>
</head>
<body>
    <!-- this is a comment node-->
    <table border="1" id="myTable">
      <tbody>
        <tr/>
        <tr>
          <td><a href="" id="myLink">Text inside anchor</a></td>
        </tr>
      </tbody>
    </table>

    <div id="results">Results:<br/></div>

<button onclick="findNodes()">Find Nodes</button>
<button onclick="refresh()">Reload</button>
</body>
</html>
```

## Usage

     Use the filter property to exclude/include Nodes from the Iteration.

## Notes

-   Appending content to the document while the [**TreeWalker**](/dom/TreeWalker) is searching for nodes can cause an endless loop. To prevent this, the example collects all possible output in a temporary variable and appends it to the document after the **TreeWalker** is finished.
-   The **NodeFilter** is a callback function that provides customized filtering for [**NodeIterator**](/dom/NodeIterator) and [**TreeWalker**](/dom/TreeWalker). The filter function accepts a node as its only parameter, and indicates whether the node is accepted, rejected, or skipped.

<!-- -->

    function myFilter(node) {
        // NodeFilter function that returns one of the following flags:
        // NodeFilter.FILTER_ACCEPT, NodeFilter.FILTER_REJECT, NodeFilter.FILTER_SKIP
    }

## Related specifications

[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/)
:   Recommendation
