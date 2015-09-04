---
title: nextNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set.  The first call to nextNode() returns the first node in the set.\n"
uri: dom/NodeIterator/nextNode

---
# nextNode

## Summary

The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set. The first call to nextNode() returns the first node in the set.

This method returns null when there are no nodes left in the set.

*Method of [dom/NodeIterator](/dom/NodeIterator)*

## Syntax

``` {.js}
var object = object.nextNode(/* see parameter list */);
```

## Parameters

### oNode

 Data-typeÂ
:   any

 Object containing the next node in the list.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
InvalidStateError \_ERR
:   NodeIterator raises this exception if detach has been invoked on the object.

Â

[**Node**](/dom/Node)

Object containing the next node in the list.

## Examples

``` {.html}
<!DOCTYPE html>
<html>
<head>
<title>NextNode example</title>
  <script type="text/javascript">
    function LoseMondays(){
      var ni = document.createNodeIterator(document.body, NodeFilter.SHOW_TEXT, null, false);
      var txt = ni.nextNode();      //go to first node of our NodeIterator
      while (txt)                   //while text
        {
          if (txt.wholeText.match('Monday') || txt.parentNode.getAttribute('id') == 'Monday')
            {
            txt.parentNode.removeChild(txt);        //remove monday's activity
            }
          txt=ni.nextNode();                        //go to next node
        }
    }
    function refresh()
      {
        window.location.reload( false );           //reload our page
      }
  </script>
</head>
<body>
    <p><strong>Harry's weekly diary</strong></p>
    <p>Monday Joe bought a turkey.</p>
    <p>Tuesday Bill bought a pound of ham.</p>
    <div>Chuck called in sick Monday.</div>
    <p id="Monday">CALL supplier today</p>
    <p>Wednesday's delivery was delayed.</p>
    <input type="button" name="reset" value="refresh" onclick="refresh()"/>
    <input type="button" name="cutmonday" value="Lose Mondays" onclick="LoseMondays()"/>
</body>
</html>
```

## Notes

### Remarks

This example shows how to create a [**NodeIterator**](/dom/NodeIterator) and move forward through the list of nodes.

### Syntax

node = nodeIterator.nextNode();

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-nextnode)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.nextNode](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.nextNode) Article]

Portions of this content come from the Microsoft Developer Network: [[nextNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975281(v=vs.85).aspx) Article]

