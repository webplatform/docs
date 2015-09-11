---
title: border-image-outset
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/border-image-outset)'
code_samples:
  - 'http://gist.github.com/5622268'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'all elements, except internal table elements when `border-collapse` is set to `collapse`.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'all length made absolute, otherwise as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderImageOutset`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The border-image-outset property describes, by which amount the border image area extends beyond the border box.'
tags:
  - CSS
  - Properties
uri: css/properties/border-image-outset

---
## <span>Summary</span>

The border-image-outset property describes, by which amount the border image area extends beyond the border box.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   all elements, except internal table elements when `border-collapse` is set to `collapse`.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   all length made absolute, otherwise as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderImageOutset`

Percentages
:   N/A

## <span>Syntax</span>

-   `border-image-outset: <length>`
-   `border-image-outset: inherit`

## <span>Values</span>

\<length\>
:   Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length). This length must not be negative.

inherit
:   Is a keyword indicating that all four values are inherited from their parent's element calculated value.

## <span>Examples</span>

A simple example showing multiple \<div\>s, identical in style except that they have different border-image-outset properties applied to them.

``` html
<div class="pattern one">one</div>
<div class="pattern two">two</div>
<div class="pattern three">three</div>
<div class="pattern four">four</div>
```

[View live example](http://code.webplatform.org/gist/5622268)

``` css
/* This general class will apply the pattern to the containers */
.pattern {
    border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
    border-image-slice: 30;
    border-image-width: 6;
    border-image-repeat: repeat;

}

/* One-value syntax */
.pattern.one{
    border-image-outset: 3;
}

/* Two-value syntax */
.pattern.two{
    border-image-outset: 1.2em 1.8em;
}

/* Three-value syntax */
.pattern.three{
    border-image-outset: 5px 3px 10px;
}

/* Four-value syntax */
.pattern.four{
    border-image-outset: 5 2em 10 3px;
}
```

[View live example](http://code.webplatform.org/gist/5622268)

## <span>Usage</span>

     * Up to four different values can be specified, in the following order: top, right, bottom, left.

-   If one value is specified, it is used for all four sides. If two values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three values are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.

## <span>Related specifications</span>

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-image-outset)
:   W3C Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Border</span>

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   **border-image-outset**

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)

### <span>Other articles</span>

-   [Decorating fancy borders with CSS border-image](/tutorials/css_border_image)
