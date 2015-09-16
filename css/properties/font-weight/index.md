---
title: 'font-weight'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/font-weight)'
code_samples:
  - 'http://gist.github.com/5628518'
compatibility:
  feature: font-weight
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'The keyword or the numerical value as specified, with bolder and lighter transformed to the real value.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontWeight`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The font-weight property specifies the weight or boldness of the font (their degree of blackness or stroke thickness). Note that some fonts are not available in all weights; some are available only on normal and bold.'
tags:
  - CSS
  - Properties
uri: css/properties/font-weight

---
## Summary

The font-weight property specifies the weight or boldness of the font (their degree of blackness or stroke thickness). Note that some fonts are not available in all weights; some are available only on normal and bold.

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
:   The keyword or the numerical value as specified, with bolder and lighter transformed to the real value.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `fontWeight`

Percentages
:   N/A

## Syntax

-   `font-weight: 100, 200, 300, 400, 500, 600, 700, 800, 900`
-   `font-weight: bold`
-   `font-weight: bolder`
-   `font-weight: lighter`
-   `font-weight: normal`

## Values

normal
:   Normal font weight. Same as **400**.

bold
:   Bold font weight. Same as **700**.

lighter
:   One font weight lighter than the parent element (among the available weights of the font).

bolder
:   One font weight darker than the parent element (among the available weights of the font).

100, 200, 300, 400, 500, 600, 700, 800, 900
:   Numeric font weights for fonts that provide more than just normal and bold. If the exact weight given is unavailable, a face with a nearby weight is used.

## Examples

A selection of examples showing some typical uses of the font-weight property. In practise, you most probably won't see much difference when using any values except for `normal` and `bold`.

``` html
<p class="example-one">Set text to be bold.</p>
<p class="example-two">Set text to two step darker than normal but less than a standard bold.</p>
<p class="example-three">Sets text to be one step lighter than the parent.</p>
```

``` css
p { font-size: 150%; }

p.example-one { font-weight: bold; }
p.example-two { font-weight: 600; }
p.example-three { font-weight: lighter; }
```

[View live example](http://code.webplatform.org/gist/5628518)

## Usage

     Quite often there are only a few weights available for a particular font family. When a weight is specified for which no face exists, a face with a nearby weight is used:

**600-900** use the closest available darker weight (or, if there is none, the closest available lighter weight).
**100-500** use the closest available lighter weight (or, if there is none, the closest available darker weight).
 This means that for fonts that provide only normal and bold, **100-500** are normal, and **600-900** are bold.

Although the practice — also called “Faux bold” — is not well-loved by typographers, bold faces are often synthesized by user agents for faces that lack actual bold faces.

**100** to **900**
 These values form an ordered sequence, where each number indicates a weight that is at least as dark as its predecessor. These roughly correspond to the commonly used weight names below:

-   **100** - Thin
-   **200** - Extra Light (Ultra Light)
-   **300** - Light
-   **400** - Normal
-   **500** - Medium
-   **600** - Semi Bold (Demi Bold)
-   **700** - Bold
-   **800** - Extra Bold (Ultra Bold)
-   **900** - Black (Heavy)

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#font-weight-prop)
:   W3C Working Draft

[CSS Transitions](http://www.w3.org/TR/css3-transitions/#animatable-css)
:   W3C Working Draft

## See also

### External resources

-   A List Apart: [Say No to Faux Bold](http://alistapart.com/article/say-no-to-faux-bold)
-   Mozilla: [default style sheet](http://mxr.mozilla.org/mozilla/source/layout/style/html.css)
-   WebKit: [default style sheet](http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css)
-   IECSS: [Internet Explorer User Agent Style Sheets](http://www.iecss.com/)
