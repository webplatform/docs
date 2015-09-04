---
title: queryCommandSupported
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Returns a Boolean value that indicates whether the current command is supported on the current range.'
uri: dom/TextRange/queryCommandSupported

---
# queryCommandSupported

## Summary

Returns a Boolean value that indicates whether the current command is supported on the current range.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var result = document.queryCommandSupported(/* see parameter list */);
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
:   The command is supported.
false
:   The command is not supported.

Â

## Examples

The follow example uses window.getSelection feature testing and if it is not supported by the client browser falls back to document.selection. 'queryCommandSupported' is then used on the range object to determine if the 'bold' command is supported in the current context.

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
        if(rng.queryCommandSupported('bold')){
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

Portions of this content come from the Microsoft Developer Network: [[queryCommandSupported Method](http://msdn.microsoft.com/en-us/library/ie/ms536681(v=vs.85).aspx) Article]

