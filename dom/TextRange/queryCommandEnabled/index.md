---
title: queryCommandEnabled
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.'
uri: dom/TextRange/queryCommandEnabled

---
# queryCommandEnabled

## Summary

Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var Result = document.queryCommandEnabled(/* see parameter list */);
```

## Parameters

### cmdID

 Data-typeÂ
:   BSTR

**String**Â that specifies a command identifier.

see [dottoro.com](http://help.dottoro.com/larpvnhw.php) for a full listing of commands.

## Return Value

Returns an object of type Boolean.

Boolean

**Boolean** that returns one of the following possible values:

Return value
:   Description
true
:   The command is enabled.
false
:   The command is disabled.

Â

## Examples

The following example is a onClick handler to execute the 'cut' command.

``` {.js}
function execCut(){
if(document.queryCommandEnabled('cut')){
    document.execCommand('cut',false,null);}
}
```

## Notes

### Remarks

Using **queryCommandEnabled** ("delete") on a [**TextRange**](/dom/TextRange) object returns true, while **queryCommandEnabled** ("delete") on a [Document](/dom/Document) object returns false. However, **execCommand** ("delete") can still be used to delete the selected text. This method is a wrapper function for the command constants. You can obtain an **IHTMLDocument2** interface using IID\_IHTMLDocument2 for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLControlRange** interface using IID\_IHTMLControlRange for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLTxtRange** interface using IID\_IHTMLTxtRange for the IID.

## See also

### Other articles

[help.dottoro.com - Command Reference](http://help.dottoro.com/larpvnhw.php)

[MSDN Commands A-Z](http://msdn.microsoft.com/en-us/library/ie/hh801227(v=vs.85).aspx)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[queryCommandEnabled Method](http://msdn.microsoft.com/en-us/library/ie/ms536676(v=vs.85).aspx) Article]

