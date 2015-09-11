---
title: cloneNode
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.cloneNode](https://developer.mozilla.org/en-US/docs/Web/API/Node.cloneNode) Article]'
  - 'Microsoft Developer Network: [[cloneNode Method](http://msdn.microsoft.com/en-us/library/ie/ms536365(v=vs.85).aspx) Article]'
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
summary: 'Copies a reference to the object from the document hierarchy.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/cloneNode

---
## <span>Summary</span>

Copies a reference to the object from the document hierarchy.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var clonedNode = node.cloneNode(/* see parameter list */);
```

## <span>Parameters</span>

### <span>cloneDescendants</span>

 Data-type
:   Boolean

 Whether to clone the child nodes of the node as well.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The cloned node.

## <span>Examples</span>

``` html
<!doctype html>
<script>
function fnClone(){
   /* the 'true' possible value specifies to clone
      the childNodes as well.
   */
   var oCloneNode = document.getElementById("oList").cloneNode(true);
   /* When the cloned node is added,
   'oList' becomes a collection.
   */
   document.body.insertBefore(oCloneNode);
}
</script>
<ul id="oList">
<li>List node 1</li>
<li>List node 2</li>
<li>List node 3</li>
<li>List node 4</li>
</ul>
<input type="button" value="Clone List" onclick="fnClone()">
```

## <span>Usage</span>

     Use this method to copy an node, its attributes and, if specified, its childNodes as well.

## <span>Notes</span>

When you refer to the **id** of a cloned element, a collection is returned. **cloneNode**does not work on an **IFRAME** directly. You must call **cloneNode**through the **all** collection. The following example demonstrates how to call **cloneNode** on an **iframe**.

    <!doctype html>

\<html\>

    <script>
    function fnBegin(){
        var fr = document.getElementByid("oFrame").cloneNode();
        console.log(document.body.innerHTML);
    }
    </script>
    <body onload="fnBegin()">
        <iframe id="oFrame" src="about:blank"
            style="border:1px solid black; position:absolute; top:20px; left:30px;
                width:350px; height:300px;"></iframe>
    </body>
    </html>

If the object being cloned is an element and that element has expandos defined on it, the expandos are copied to the clone when **cloneNode** is called. Other browsers might handle this differently.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
