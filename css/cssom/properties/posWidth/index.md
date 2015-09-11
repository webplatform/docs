---
title: posWidth
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
summary: 'Reflects the value of the Cascading Style Sheets (CSS) width attribute for positioned items.'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/cssom/properties/posWidth

---
## <span>Summary</span>

Reflects the value of the Cascading Style Sheets (CSS) width attribute for positioned items.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## <span>Syntax</span>

``` js
var result = element.posWidth;
element.posWidth = value;
```

## <span>Examples</span>

This example uses the **posWidth** property to increase the width of the first **img** object by 10 units.

``` js
<SCRIPT LANGUAGE="JScript">
document.all.tags("IMG").item(0).style.posWidth += 10;
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

This property reflects the value of the Cascading Style Sheets (CSS) [**width**](/css/properties/width) attribute for positioned items. This property always returns zero for nonpositioned items because "width" has meaning only when the object is positioned. If the **width** attribute is not set, the **posWidth** property returns zero. Setting the **posWidth** property changes the value of the width but leaves the units designator for the property unchanged. Unlike the [**width**](/css/properties/width) property, the **posWidth** property value is a floating-point number, not a string.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `defaults`
-   `runtimeStyle`
-   `style`
-   `pixelWidth`
