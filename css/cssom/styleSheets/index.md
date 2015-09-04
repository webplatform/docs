---
title: styleSheets
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs spec reference, standardization status'
summary: 'A collection of the document''s stylesheets.'
uri: css/cssom/styleSheets

---
# styleSheets

## Summary

A collection of the document's stylesheets.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example shows how to display the titles of the style sheets in the document.

``` {.js}
for ( i = 0; i < document.styleSheets.length; i++ )
{
    alert("Style sheet " + i + " is titled " + document.styleSheets(i).title);
}
```

## Notes

### Remarks

Style sheets that are imported using the [**@import**](/css/atrules/@import) rule and are contained within the **style** object are available through the [**imports**](/css/cssom/imports) collection.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

