---
title: getAdjacentText
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec and compat table'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Element
standardization_status: Non-Standard
summary: 'Non standard. Gets a text from a given location around the edges of the element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/getAdjacentText

---
## Summary

Non standard. Gets a text from a given location around the edges of the element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var text = element.getAdjacentText(where);
```

## Parameters

### where

 Data-type
:   String

 Where the text is located by using one of the following values.

**beforeBegin**

Text is returned immediately before the element.

**afterBegin**

Text is returned after the start of the element but before all other content in the element.

**beforeEnd**

Text is returned immediately before the end of the element but after all other content in the element.

**afterEnd**

Text is returned immediately after the end of the element.

## Return Value

Returns an object of type StringString

The first adjacent text.

## Examples

This example uses the **getAdjacentText** method to find specific text.

``` html
<script>
function findText(){
        var select = document.getElementById("sel");
    var whereToFind = select.options[select.selectedIndex].textContent;
    console.log(document.getElementById("para").getAdjacentText(whereToFind));
}
</script>
This is the text before (beforeBegin).
<p id="para">
This is the text after (afterBegin).
<b>A few extra words.</b>
This is the text before (beforeEnd).
</p>
This is the text after (afterEnd).
<select id="sel">
<option selected="selected">beforeBegin</option&gtl
<option>afterBegin</option&gtl
<option>beforeEnd</option&gtl
<option>afterEnd</option&gtl
</select>
<input type="button" value="Find text" onclick="findText()">
```

