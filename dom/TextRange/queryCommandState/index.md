---
title: queryCommandState
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Returns a Boolean value that indicates the current state of the command.'
uri: dom/TextRange/queryCommandState

---
# queryCommandState

## Summary

Returns a Boolean value that indicates the current state of the command.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var result = document.queryCommandState(/* see parameter list */);
```

## Parameters

### cmdID

 Data-typeÂ
:   BSTR

**String**Â that specifies a command identifier.

## Return Value

Returns an object of type Boolean.

Boolean

**Boolean** that returns one of the following possible values:

Return value
:   Description
true
:   The given command has been executed on the object.
false
:   The given command has not been executed on the object.

Â

## Examples

This example feature tests for window.getSelection and if not available (legacy IE versions) falls back to document.selection to create a range object. Then queryCommandState is used to determine if the range object can execute the 'bold' command.

``` {.js}
function makeBold(el){
if(window.getSelection){
    var sel=document.getSelection();
    var range = sel.getRangeAt(0),
    content = range.extractContents(),
    span = document.createElement('b');
    span.appendChild(content);
    var htmlContent = span.innerHTML;
    range.insertNode(span);
}else{
    var sel=document.selection;
    if(sel){
        var rng=sel.createRange();
        if(rng.queryCommandEnabled('bold')){rng.execCommand('bold',false,null);}
    }
}
}
```

## Usage

     Used to add HTML markup to web documents.

## Notes

### Remarks

This method is a wrapper function for the command constants. You can obtain an **IHTMLDocument2** interface using IID\_IHTMLDocument2 for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLControlRange** interface using IID\_IHTMLControlRange for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLTxtRange** interface using IID\_IHTMLTxtRange for the IID.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[queryCommandState Method](http://msdn.microsoft.com/en-us/library/ie/ms536679(v=vs.85).aspx) Article]

