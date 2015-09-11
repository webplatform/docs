---
title: styleSheets
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'In Progress'
summary: 'A collection of the document''s stylesheets.'
tags:
  - API
  - Objects
  - DOM
uri: css/cssom/styleSheets

---
## <span>Summary</span>

A collection of the document's stylesheets.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

This example shows how to display the titles of the style sheets in the document.

``` js
for ( i = 0; i < document.styleSheets.length; i++ )
{
    alert("Style sheet " + i + " is titled " + document.styleSheets(i).title);
}
```

## <span>Notes</span>

### <span>Remarks</span>

Style sheets that are imported using the [**@import**](/css/atrules/@import) rule and are contained within the **style** object are available through the [**imports**](/css/cssom/imports) collection.