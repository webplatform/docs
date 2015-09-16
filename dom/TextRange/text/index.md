---
title: text
attributions:
  - 'Microsoft Developer Network: [[text Property](http://msdn.microsoft.com/en-us/library/ie/ms534676(v=vs.85).aspx) Article]'
notes:
  - 'Not sure if a standard applies here.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TextRange
    href: /dom/TextRange
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/TextRange
standardization_status: Mixed
summary: 'Sets or retrieves the text contained within the range. '
tags:
  - API
  - Object
  - Properties
uri: dom/TextRange/text

---
## Summary

Sets or retrieves the text contained within the range.

Property of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var result = textRange.text;
textRange.text = value;
```

## Return Value

Returns an object of type StringString

the contained text.

## Examples

The following example feature tests for getSelection support and extracts the text contained within the bounds of the range(s) object(s).

``` js
function showText(){
if(window.getSelection){
    var buf='';
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

