---
title: queryCommandIndeterm
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Returns a Boolean value that indicates whether the specified command is in the indeterminate state.'
uri: dom/TextRange/queryCommandIndeterm

---
# queryCommandIndeterm

## Summary

Returns a Boolean value that indicates whether the specified command is in the indeterminate state.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var Result = document.queryCommandIndeterm(/* see parameter list */);
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
:   The command is in the indeterminate state.
false
:   The command is not in the indeterminate state.

Â

## Examples

``` {.js}
function SetToBold () {
            if (document.queryCommandIndeterm ("bold")) {
                alert ("The 'bold' command is in an indeterminate state.");
            }
            else {
                if (document.queryCommandState ("bold")) {
                    alert ("The bold formatting will be removed from the selected text.");
                }
                else {
                    alert ("The selected text will be displayed in bold.");
                }
            }
            document.execCommand ('bold', false, null);
        }
```

## Notes

### Remarks

This method is a wrapper function for the command constants. You can obtain an **IHTMLDocument2** interface using IID\_IHTMLDocument2 for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLControlRange** interface using IID\_IHTMLControlRange for the IID. This method is a wrapper function for the command constants. You can obtain an **IHTMLTxtRange** interface using IID\_IHTMLTxtRange for the IID.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[queryCommandIndeterm Method](http://msdn.microsoft.com/en-us/library/ie/ms536678(v=vs.85).aspx) Article]

