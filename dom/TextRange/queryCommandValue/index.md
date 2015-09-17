---
title: 'queryCommandValue'
attributions:
  - 'Microsoft Developer Network: [[queryCommandValue Method](http://msdn.microsoft.com/en-us/library/ie/ms536683(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Returns the current value of the document, range, or current selection for the given command.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/TextRange/queryCommandValue

---
## Summary

Returns the current value of the document, range, or current selection for the given command.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var object = document.queryCommandValue(/* see parameter list */);
```

## Parameters

### cmdID

 Data-type
:   BSTR

**String** that specifies a command identifier.

## Return Value

Returns an object of type DOM NodeDOM Node

Variant

**Variant** that returns the command value for the document, range, or current selection, if supported. Possible values depend on *cmdID*. If not supported, this method returns a **Variant** of type **Boolean** set to false.

## Examples

The following example when using legacy document.selection will display an alert message of 'false' if the current selection is not 'bold', or true if it is already 'bold'

``` js
function makeBold(el){
if(window.getSelection){
    var sel=document.getSelection();
    var range= sel.getRangeAt(0),
    content = range.extractContents(),
    span = document.createElement('b');
    span.appendChild(content);
    var htmlContent = span.innerHTML;
    range.insertNode(span);
}else{
    var sel=document.selection;
    if(sel){
        var rng=sel.createRange();
        alert(rng.queryCommandValue('bold'));
// true if the rng is 'bold' already, false otherwise.
        if(rng.queryCommandSupported('bold')){
            if(rng.queryCommandEnabled('bold')){rng.execCommand('bold',false,null);}
        }
    }
}
}
```

## Usage

     Used for changing the HTML markup of web pages.

## Notes

### Remarks

This method is a wrapper function for the command constants. You can obtain an **IHTMLDocument2** interface using IID\_IHTMLDocument2 for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLControlRange** interface using IID\_IHTMLControlRange for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLTxtRange** interface using IID\_IHTMLTxtRange for the IID.
