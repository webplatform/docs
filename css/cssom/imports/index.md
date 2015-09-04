---
title: imports
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status'
uri: css/cssom/imports

---
# imports

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example shows how to display the URL paths of the imported style sheets in the document.

``` {.js}
for ( i = 0; i < document.styleSheets.length; i++ )
{
    if ( document.styleSheets(i).owningElement.tagName == "STYLE" )
    {
        for ( j = 0; j < document.styleSheets(i).imports.length; j++ )
            alert("Imported style sheet " + j + " is at " +
                   document.styleSheets(i).imports(j).href);
    }
}
```

## Notes

### Remarks

An imported style sheet is one that is brought into the document using the cascading style sheets (CSS) [**@import**](/css/atrules/@import) rule.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

