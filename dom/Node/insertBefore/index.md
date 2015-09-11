---
title: insertBefore
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.insertBefore](https://developer.mozilla.org/en-US/docs/Web/API/Node.insertBefore) Article]'
  - 'Microsoft Developer Network: [[insertBefore Method](http://msdn.microsoft.com/en-us/library/ie/ms536454(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertBefore.htm'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Inserts a child into the node, immediately before the specified reference child node.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/insertBefore

---
## <span>Summary</span>

Inserts a child into the node, immediately before the specified reference child node.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var insertedNode = node.insertBefore(/* see parameter list */);
```

## <span>Parameters</span>

### <span>newNode</span>

 Data-type
:   DOM Node

 The new node to be inserted.

### <span>refChild</span>

 Data-type
:   DOM Node

(Optional)

Supplies the placement of the new node. If this parameter is specified, the new element will be inserted immediately before this existing child node. If not, it will be added after the last child node.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The inserted node.

## <span>Examples</span>

The following example shows how to use the **insertBefore** method to insert a new item into an existing list.

``` html
<!doctype html>
<html>
<head>
<script type="application/javascript">
    function insertElement()
    {
        var nod=document.createElement("li");
        document.getElementById("oUL1").insertBefore(nod, document.getElementById("oLIYellow"));
        nod.textContet="Orange";
    }
</script>
</head>
<body>
    <p onclick="insertElement()">Click <strong>HERE</strong> to add an item to the following list.</p>
    <ul id="oUL1">
        <li id="oLIRed">Red</li>
        <li id="oLIYellow">Yellow</li>
        <li id="oLIBlue">Blue</li>
    </ul>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertBefore.htm)

## <span>Notes</span>

Do not specify the *refChild* parameter when inserting the first child node. If children already exist and you do not specify the *refChild* parameter, the *newChild* becomes the last child of the parent object. This method is accessible at run time. If elements are removed at run time, before the closing tag has been parsed, areas of the document might not render.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-952280727)
:   Recommendation

[DOM4](http://www.w3.org/TR/dom/#dom-node-insertbefore)
:   Working Draft
