---
title: mask-border-width
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'All \<length\>s made absolute, otherwise as specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'Relative to width/height of the mask box image area.'
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property sets the width of the mask box image, similar to the CSS border-image-width property.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-border-width

---
## <span>Summary</span>

This property sets the width of the mask box image, similar to the CSS border-image-width property.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   All \<length\>s made absolute, otherwise as specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   Relative to width/height of the mask box image area.

## <span>Syntax</span>

-   `mask-border-width: auto`
-   `mask-border-width: length`
-   `mask-border-width: number`
-   `mask-border-width: percentage`

## <span>Values</span>

auto
:   If specified, the mask box image width is the intrinsic width or height (whichever is applicable) of the corresponding image slice (see [mask-border-slice](/css/properties/mask-border-slice)). If the image does not have the required intrinsic dimension then the corresponding *border-width* is used.

length
:   Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.

percentage
:   Refers to the size of the mask border image area: the width of the area for horizontal offsets, the height for vertical offsets.

number
:   Represents multiples of the corresponding computed *border-width*.

## <span>Examples</span>

``` css
/* auto */
#maskbox1: {
    mask-border-width: auto;
}

/* percentage */
#maskbox2: {
    mask-border-width: 5%;
}
```

``` css
.exampleone {
    -webkit-mask-border: url('mask.png');
}

.exampletwo {
    -webkit-mask-border: url('logo.png') 100 100 0 0 round round;
}
```

## <span>Related specifications</span>

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft
