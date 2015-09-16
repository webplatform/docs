---
title: 'counter-reset'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5841988'
compatibility:
  feature: counter-reset
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
summary: 'The counter-reset property contains a list of one or more names of counters, each one optionally followed by an integer (otherwise, the integer defaults to 0.)  Each time the given element is invoked, the counters specified by the property are set to the given integer.'
tags:
  - CSS
  - Properties
uri: css/properties/counter-reset

---
## Summary

The counter-reset property contains a list of one or more names of counters, each one optionally followed by an integer (otherwise, the integer defaults to 0.) Each time the given element is invoked, the counters specified by the property are set to the given integer.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `counter-reset: identifier`
-   `counter-reset: integer`

## Values

identifier
:   The name of the counter, optionally followed by an integer.

integer
:   The value to which the counter is set when the element is invoked. The default value is 0.

## Examples

The following example demonstrates automatic chapter and section numbering using **counter-reset**, [**counter-increment**](/css/properties/counter-increment), and [**content**](/css/properties/content). The `chapter` counter is set to zero for the **body** element, and then incremented for each **h1** element encountered. The `section` counter is reset for each **h1** element and incremented for each **h2** element. When the page is viewed, each **h1** element is preceded by a chapter heading of the form `"Chapter`*X*`."`, while each **h2** element is preceded by a section number of the form `"`*X.N*`"`.

``` css
body {
    counter-reset: chapter;      /* Create a chapter counter */
}
h1 {
    counter-increment: chapter;  /* Add 1 to chapter */
    counter-reset: section;      /* Set section to 0 */
}
h1:before {
    content: "Chapter " counter(chapter) ". ";
}
h2 {
    counter-increment: section;
}
h2:before {
    content: counter(chapter) "." counter(section) " ";
}
```

[View live example](http://code.webplatform.org/gist/5841988)

## Notes

### Remarks

The **counter-reset** attribute can contain a list of one or more counters, each one optionally followed by an integer. The integer represents the value that the counter is set to after each occurrence of the element. If an element both resets and increments a counter, the counter is reset first and then incremented. If the same counter is specified more than once, each reset or increment of the counter is processed in the order specified. The [**counter-increment**](/css/properties/counter-increment) and **counter-reset** attributes follow the rules of the CSS cascade. Given two style declarations with the same specificity, only the last one encountered will be processed. For more information about cascade and specificity, see Understanding CSS Selectors. An element that is not displayed ([**display**](/css/properties/display) attribute set to 'none') and pseudo-elements that do not generate content ([**content**](/css/properties/content) attribute set to 'normal') cannot increment or reset a counter. This property requires Windows Internet Explorer to be in IE8 Standards mode rendering.

### Syntax

`counter-reset: '[  <identifier>   <integer>  ]'+`

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 12.4

## See also

### Related articles

#### Generated and Replaced Content

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   [content](/css/properties/content)

-   [counter-increment](/css/properties/counter-increment)

-   **counter-reset**

-   [list-style-image](/css/properties/list-style-image)

-   [list-style-type](/css/properties/list-style-type)

-   [object-fit](/css/properties/object-fit)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   counter-increment[counter-increment](/css/properties/counter-increment)
