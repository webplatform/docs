---
title: @import
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - '"Main Content" section is empty. We may want to either want to modify programmatically if subsections like @rules -> @import only are decided to only need examples and references to support the parent categories.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Imports an external style sheet.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@import

---
## <span>Summary</span>

Imports an external style sheet.

## <span>Examples</span>

The following example uses the **@import** rule to import a style sheet. For the example to work, you must replace `URL` in the example code with the address of a style sheet.

``` html
<STYLE TYPE="text/css">
    @import url("URL");
    P {color:blue}
</STYLE>
```

The following example, without `url()`, has the same effect as the previous example.

``` html
<STYLE type="text/css">
    @import "URL";
    P {color:blue}
</STYLE>
```

## <span>Notes</span>

### <span>Remarks</span>

The rule has no default value. The semicolon in the syntax is required; if omitted, the style sheet is not imported properly and an error message is generated. "url()" is optional because there is always a URL following "@import." The **@import** rule, like the **link** element, links an external style sheet to a document. This helps the Web author establish a consistent "look" across multiple HTML pages. Whereas the **link** element specifies the name of the style sheet to import using its [**href**](/html/attributes/href) attribute, the **@import** rule specifies the style sheet definition inside a **link** element or a **style** element. In the scripting model, this means the [**owningElement**](/css/cssom/styleSheet/owningElement) property of the style sheet defined through the **@import** rule is either a **style** or a **link** object. The **@import** rule should occur at the start of a style sheet, before any declarations. You can place **@import** rule statements anywhere within the style sheet definition, but the rules contained within the **@import** rule style sheet are applied to the document before any other rules defined for the containing style sheet. This rule order affects expected rendering. Rules in the style sheet override rules in the imported style sheet.

### <span>Syntax</span>

@import

### <span>Parameters</span>

*sUrl*
:   String that specifies the URL that references a cascading style sheet.

## <span>Related specifications</span>

[CSS Cascading and Inheritance Level 3](http://www.w3.org/TR/css3-cascade/)
:   W3C Working Draft

[CSS 2.1, section 6.3](http://www.w3.org/TR/CSS2/cascade.html#at-import)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   **@import**

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### <span>Syntax</span>

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   **@import**

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)

### <span>Related pages</span>

-   `imports`
-   `:link`
-   `style`
-   `styleSheet`
