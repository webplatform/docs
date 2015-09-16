---
title: 'word-break'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6392109'
compatibility:
  feature: word-break
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`wordBreak`'
  Percentages: 'Not available'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The word-break property is often used when there is long generated content that is strung together without and spaces or hyphens to beak apart. A common case of this is when there is a long URL that does not have any hyphens. This case could potentially cause the breaking of the layout as it could extend past the parent element.'
tags:
  - CSS
  - Properties
uri: css/properties/word-break

---
## Summary

The word-break property is often used when there is long generated content that is strung together without and spaces or hyphens to beak apart. A common case of this is when there is a long URL that does not have any hyphens. This case could potentially cause the breaking of the layout as it could extend past the parent element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `wordBreak`

Percentages
:   Not available

## Syntax

-   `word-break: break-all`
-   `word-break: keep-all`
-   `word-break: normal`

## Values

normal
:   Default property. Words break according to their usual rules.

break-all
:   In addition to `normal` soft wrap opportunities, lines may break between any two letters (except where forbidden by the [**line-break**](/css/properties/line-break) property). Hyphenation is not applied. This option is used mostly in a context where the text is predominantly using CJK (Chinese/Japanese/Korean) characters with few non-CJK excerpts and it is desired that the text be better distributed on each line.

keep-all
:   Implicit soft wrap opportunities between letters are suppressed, i.e. breaks are prohibited between pairs of letters (except where opportunities exist due to dictionary-based breaking). Otherwise this option is equivalent to `normal`. In this style, sequences of CJK characters do not break.

## Examples

A simple example showing multiple `<div>`s, identical in style except that they have different `word-break` properties applied to them.

``` html
<p>This example using break-all will stay within the box border.</p>
<div class="break-all">
  http://www.exampleurl.com/this-is-a-long-url/it-will-not-break-at-hypens
</div>

<p>This example using keep-all will break where there are hyphens.</p>
<div class="keep-all">
  http://www.exampleurl.com/this-is-a-long-url/it-will-break-at-hypens
</div>
```

[View live example](http://code.webplatform.org/gist/6392109)

``` css
div {
  background: yellow;
  border: 1px solid #444;
  margin: 1em;
  padding: .5em;
  width: 200px;
  font-family: sans-serif;
}

.break-all {
  word-break: break-all;
}

.keep-all {
  word-break: keep-all;
}
```

[View live example](http://code.webplatform.org/gist/6392109)

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-word-break** attribute is an extension to CSS, and can be used as a synonym for **word-break** in IE8 Standards mode. When using the **-ms-word-break** attribute with a [**table**](/html/elements/table), you must set the [**table-layout**](/css/properties/table-layout) attribute to **fixed** on the **table**. The behaviors of the parameter values are detailed in [CSS Text Level 3: W3C Working Draft (6 March 2007), sec. 4.1, "Line Breaking Restrictions: The 'word-break' Property"](http://go.microsoft.com/fwlink/p/?linkid=203753); and in [Unicode Standard Annex \#14: Line Breaking Properties](http://go.microsoft.com/fwlink/p/?linkid=203714).

### Syntax

`word-break: normal | break-all | keep-all`

### Standards information

-   [CSS Text Module Level 3 - word-break property](http://www.w3.org/TR/css3-text/#word-break)
-   [CSS Text Level 3](http://go.microsoft.com/fwlink/p/?linkid=203766), Section 5.2
-   [Unicode Standard Annex \#14 -- Unicode Line Breaking Algorithm](http://go.microsoft.com/fwlink/p/?linkid=223137)

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   W3C Last Call Working Draft
