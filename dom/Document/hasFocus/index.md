---
title: 'hasFocus'
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
    value: Boolean
    href: /dom/Document
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns the focus state of the current document, true if the document has focus, false if not.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/hasFocus

---
## Summary

Returns the focus state of the current document, true if the document has focus, false if not.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var boolean = document.hasFocus();
```

## Return Value

Returns an object of type BooleanBoolean

Returns true if the document has focus, otherwise returns false

## Examples

The following example shows how to use the **hasFocus** method to determine if the document has focus. If you mouse over the text when the document has focus, "A message for you!" appears; if you mouse over the text when the document does not have focus, the message does not appear.

``` html
<!DOCTYPE HTML>
<html>
<head>
<script>
// Function displays the message DIV when the main document has focus
function fnOpenMessage()
{
    if (document.hasFocus())
    {
        oMessageDiv.style.display = "block";
    }
}
function fnCloseMessage()
{
    oMessageDiv.style.display = "none";
}
</script>
</head>
<body>

<p>
<span style= "color:darkmagenta;font-size:large;" onmouseout="fnCloseMessage();"
onmouseover="fnOpenMessage();">Mouse over this!</span>
</p>

<div id="oMessageDiv" style="display:none; font-family:arial; width:200px; font-size:large; color:steelblue; border:4px solid gold;">
A message for you!
</div>

</body>
</html>
```

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/editing.html#dom-document-hasfocus)
:   Candidate Recommendation
