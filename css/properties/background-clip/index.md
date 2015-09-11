---
title: background-clip
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`border-box`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backgroundClip`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies how an element’s background is clipped.'
tags:
  - CSS
  - Properties
uri: css/properties/background-clip

---
## <span>Summary</span>

Specifies how an element’s background is clipped.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `border-box`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundClip`

Percentages
:   N/A

## <span>Syntax</span>

-   `background-clip: border-box`
-   `background-clip: content-box`
-   `background-clip: padding-box`

## <span>Values</span>

border-box
:   Default. The background extends underneath the element’s borders, which can be seen with semi-transparent or dotted or dashed border-styles.

padding-box
:   The background is clipped to the padding-box, i.e. it cannot be seen under the element’s borders.

content-box
:   The background is clipped the element’s content box, so the paddings and borders have no background. This is mainly useful with multiple backgrounds with different background-clip values.

## <span>Examples</span>

The background will not extend underneath the semi-transparent black border, so the element’s borders will allow whatever is underneath the element to show through.

``` css
div
{
   border: 5px solid rgba(0,0,0,.5);
   background: deeppink;
   background-clip: padding-box;
}
```

## <span>Related specifications</span>

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#the-background-clip)
:   W3C Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Background</span>

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   **background-clip**

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
