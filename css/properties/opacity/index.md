---
title: opacity
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842705'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '[[Computed value::The same as the specified value after clipping the \<alphavalue\> to the range [0.0,1.0]]]'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`opacity`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The opacity property controls transparency and opacity of an element. Its values range from 0 to 1. Assuming defaults at parent level, an element with an opacity of 1 is completely opaque, whereas and element with an opacity of 0 is completely transparent. The opacity used when rendering an element is the product of its opacity and the opacity of its ancestors.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/opacity

---
## <span>Summary</span>

The opacity property controls transparency and opacity of an element. Its values range from 0 to 1. Assuming defaults at parent level, an element with an opacity of 1 is completely opaque, whereas and element with an opacity of 0 is completely transparent. The opacity used when rendering an element is the product of its opacity and the opacity of its ancestors.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `1`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   [[Computed value::The same as the specified value after clipping the \<alphavalue\> to the range [0.0,1.0]]]

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `opacity`

Percentages
:   N/A

## <span>Syntax</span>

-   `opacity: alpha-value`
-   `opacity: inherit`

## <span>Values</span>

alpha-value
:   A **floating-point** value between 0.0 (fully transparent) and 1.0 (fully opaque), inclusive. Any values outside the range will be clamped to this range.

inherit
:   Indicates that the property takes the same computed value as the property for the element's parent.

## <span>Examples</span>

``` css
.example1 {
  opacity: 0.5;
}
```

[View live example](http://code.webplatform.org/gist/5842705)

## <span>Usage</span>

     As an alternative to the visibility property, an element's opacity can be set to 0 to make the element take space but not appear.

It's important to note that opacity affects not only a given element, but all of the elements which it contains.

## <span>Notes</span>

The opacity setting is applied uniformly across the entire object. Any values outside the range 0.0 to 1.0 will be clamped to this range.

Object or group opacity can be thought of conceptually as a postprocessing operation. Conceptually, after the object or group is rendered into an RGBA offscreen image, the object or group opacity setting specifies how to blend the offscreen image into the current background.

Note that setting a value smaller than 1 to this property creates a new stacking context. For more information, see [What No One Told You About Z-Index](http://philipwalton.com/articles/what-no-one-told-you-about-z-index/) by Philip Walton.

## <span>Related specifications</span>

[CSS Color Module Level 3](http://www.w3.org/TR/css3-color/)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Visual Effects</span>

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [clip](/css/properties/clip)

-   [cursor](/css/properties/cursor)

-   **opacity**

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
-   `defaults`
-   `runtimeStyle`
-   `a`
