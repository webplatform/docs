---
title: posWidth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) width attribute for positioned items.'
uri: css/cssom/properties/posWidth
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# posWidth

## Summary

Reflects the value of the Cascading Style Sheets (CSS) width attribute for positioned items.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.posWidth;
element.posWidth = value;
```

## Examples

This example uses the **posWidth** property to increase the width of the first **img** object by 10 units.

``` {.js}
<SCRIPT LANGUAGE="JScript">
document.all.tags("IMG").item(0).style.posWidth += 10;
</SCRIPT>
```

## Notes

### Remarks

This property reflects the value of the Cascading Style Sheets (CSS) [**width**](/css/properties/width) attribute for positioned items. This property always returns zero for nonpositioned items because "width" has meaning only when the object is positioned. If the **width** attribute is not set, the **posWidth** property returns zero. Setting the **posWidth** property changes the value of the width but leaves the units designator for the property unchanged. Unlike the [**width**](/css/properties/width) property, the **posWidth** property value is a floating-point number, not a string.

## See also

### Related pages (MSDN)

-   `defaults`
-   `runtimeStyle`
-   `style`
-   `pixelWidth`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

