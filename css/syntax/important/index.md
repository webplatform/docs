---
title: '!important'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/a246da0a53497ae9d832'
notes:
  - 'Move candidate'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'Declarations with !important override similar declarations that are not marked as !important. This can be used in both author and user style sheets.'
tags:
  - Basic
  - Pages
uri: css/syntax/!important

---
## Summary

Declarations with !important override similar declarations that are not marked as !important. This can be used in both author and user style sheets.

## Description

CSS attempts to create a "balance of power" between author and user style sheets. By default, rules in an author's style sheet override those in a user's style sheet. However, for balance, an **!important** declaration takes precedence over a normal declaration. Both author and user style sheets may contain **!important** declarations, and user **!important** rules override author **!important** rules. Declaring a shorthand property (for instance, the [**background**](/css/properties/background) property) to be **!important** is equivalent to declaring all of its sub-properties to be **!important**.

## Syntax

` { declaration !important  }`

## Values

declaration
:   A CSS property and value declaration within a rule set.

## Examples

The first rule in the user's style sheet in the following example contains an **!important** declaration, which overrides the corresponding declaration in the author's style sheet. The second declaration will also take precedence due to being marked **!important**. However, the third rule in the user's style sheet is not **!important**, and will therefore lose to the second rule in the author's style sheet (which happens to set style on a shorthand property). Also, the third author rule will lose to the second author rule since the second rule is **!important**. This shows that **!important** declarations also have a function within author style sheets.

``` css
/* From the user's style sheet */
p { text-indent: 1em !important }
p { font-style: italic !important }
p { font-size: 18pt }
/* From the author's style sheet */
p { text-indent: 1.5em !important }
p { font: normal 12pt sans-serif !important }
p { font-size: 24pt }
```

[View live example](http://code.webplatform.org/gist/a246da0a53497ae9d832)

## Related specifications

[Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification](http://www.w3.org/TR/CSS2/cascade.html#important-rules)
:   Recommendation

## See also

### Related articles

#### Syntax

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   **!important**

