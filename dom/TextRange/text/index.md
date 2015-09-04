---
title: text
tags:
  - API
  - Object
  - Properties
readiness: 'Almost Ready'
standardization_status: Mixed
notes:
  - 'Not sure if a standard applies here.'
summary: 'Sets or retrieves the text contained within the range. '
uri: dom/TextRange/text

---
# text

## Summary

Sets or retrieves the text contained within the range.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TextRange](/dom/TextRange)</span></span>

## Syntax

``` {.js}
var result = textRange.text;
textRange.text = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

the contained text.

## Examples

The following example feature tests for getSelection support and extracts the text contained within the bounds of the range(s) object(s).

``` {.js}
function showText(){
if(window.getSelection){
    var buf=;
    var sel=document.getSelection();
    for(var I=0;i<sel.rangeCount;i++)
    {
        var range=sel.getRangeAt(i);
        buf+=range.extractContents().textContent;
    }
    alert(buf);
}else{
    var sel=document.selection;
    if(sel){
        var rng=sel.createRange();
        if(rng!=null){
            alert(rng.text);
        }
        }
}
}
```

## Usage

     Used to extract only the text content from a range.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[text Property](http://msdn.microsoft.com/en-us/library/ie/ms534676(v=vs.85).aspx) Article]

