---
title: 'pasteHTML'
attributions:
  - 'Microsoft Developer Network: [[pasteHTML Method](http://msdn.microsoft.com/en-us/library/ie/ms536656(v=vs.85).aspx) Article]'
notes:
  - 'some more examples using feature testing?'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Pastes HTML text into the given text range, replacing any previous text and HTML elements in the range.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/TextRange/pasteHTML

---
## Summary

Pastes HTML text into the given text range, replacing any previous text and HTML elements in the range.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var result = range.pasteHTML(/* see parameter list */);
```

## Parameters

### html

 Data-type
:   String

**String** that specifies the HTML text to paste. The string can contain text and any combination of the HTML tags described in HTML Elements.

## Return Value

Returns an object of type

## Examples

This example uses the **pasteHTML** method to replace the current selection with a new paragraph.

``` js
<script type="text/javascript">
if(window.getSelection){
// use standards instead
}else{
var sel = document.selection;
if (sel!=null) {
    var rng = sel.createRange();
    if (rng!=null)
        rng.pasteHTML('<p><b>Selection has been replaced</b></p>'
}
}
</script>
```

The following example uses feature detection to determine whether to use getSelection or document.selection.

``` js
function makeMark(el){
if(window.getSelection){
    var sel=document.getSelection();
    for(var i=0;i<sel.rangeCount;i++)
    {
    var range = sel.getRangeAt(i),
    content = range.extractContents(),
    span = document.createElement('mark');
    span.appendChild(content);
    var htmlContent = span.innerHTML;
    range.insertNode(span);}
}else{
    var sel=document.selection;
    if(sel){
        var rng=sel.createRange();
        if(rng!=null){
            rng.pasteHTML('<span style=\"color:black;background:yellow\">'+rng.text+'</span>');
        }
        }
}
}
```

## Notes

### Remarks

This method might alter the HTML text to make it fit the given text range. For example, pasting a table cell into a text range that does not contain a table might cause the method to insert a [**table**](/html/elements/table) element. For predictable results, paste only well-formed HTML text that fits within the given text range. This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render. This feature might not be available on non-Microsoft Win32 platforms. This method fails only when used inappropriately to paste HTML into a **TEXTAREA** element in Microsoft Internet Explorer 5 and later.
