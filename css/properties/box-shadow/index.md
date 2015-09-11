---
title: box-shadow
code_samples:
  - 'http://gist.github.com/5259244'
  - 'http://gist.github.com/5259299'
  - 'http://gist.github.com/5259449'
  - 'http://gist.github.com/5259463'
  - 'http://gist.github.com/5259501'
  - 'http://gist.github.com/5259470'
  - 'http://gist.github.com/5259531'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'any length made absolute; any specified color computed; otherwise as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`boxShadow`'
  Percentages: n/a
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The box-shadow property programmatically creates one or more shadows on the inside or outside of a block level element.'
tags:
  0: CSS
  1: Properties
  3: Design
  4: UI
  5: Usability
uri: css/properties/box-shadow

---
## <span>Summary</span>

The box-shadow property programmatically creates one or more shadows on the inside or outside of a block level element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   any length made absolute; any specified color computed; otherwise as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `boxShadow`

Percentages
:   n/a

## <span>Syntax</span>

-   `box-shadow: blur-radius (optional)`
-   `box-shadow: inset (optional)`
-   `box-shadow: offset-x (optional)`
-   `box-shadow: offset-x offset-y blur-radius color, offset-x offset-y blur-radius color`
-   `box-shadow: offset-y (optional)`
-   `box-shadow: spread-distance (optional)`

## <span>Values</span>

inset (optional)
:   If not specified (default), the shadow is assumed to be a drop shadow (as if the box were raised above the content). The presence of the `inset` keyword changes the shadow to one inside the frame (as if the content was depressed inside the box). Inset shadows are drawn inside the border (even transparent ones), above the background, but below content.

offset-x (optional)
:   The first length is the horizontal offset of the shadow — offset-x specifies the horizontal offset of the shadow, which can be a number of any length unit. Positive values place the shadow to the right of the element, and negative values to the left. If both offset-x and offset-y values are 0, the shadow is placed directly behind the element.

offset-y (optional)
:   The second length is the vertical offset of the shadow — offset-y specifies the vertical offset of the shadow, which can be a number of any length unit. Positive values place the shadow below the element, and negative values above. If both offset-x and offset-y values are 0, the shadow is placed directly behind the element.

blur-radius (optional)
:   The third length is a blur radius, which can be a number of any length unit. The larger this value, the bigger the blur, meaning the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it defaults to 0 (the shadow's edge is sharp).

spread-distance (optional)
:   The fourth length is a spread distance, which again can be a number of any unit. Positive values cause the shadow to expand and grow bigger, negative values cause the shadow to shrink. If not specified, it defaults to 0 (the shadow is the same size as the element). Note that setting the size of an outer shadow to 0 causes it to disappear, whereas a 0-sized inner shadow covers the entire padding-box. For inner shadows, expanding the shadow (creating more shadow area) means contracting the shadow's perimeter shape.

offset-x offset-y blur-radius color, offset-x offset-y blur-radius color
:   To apply multiple shadows to one element, write the `box-shadow` values out one after another, separated by commas.

## <span>Examples</span>

An example of a basic drop shadow. An outer box-shadow casts a shadow as if the border-box of the element were opaque. The shadow is drawn outside the border edge only: it is clipped inside the border-box of the element.

``` css
article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
```

[View live example](http://code.webplatform.org/gist/5259244)

An example of inner drop shadows. An inner box-shadow casts a shadow as if everything outside the padding edge were opaque. The inner shadow is drawn inside the padding edge only: it is clipped outside the padding box of the element.

``` css
article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5) inset;
}
```

[View live example](http://code.webplatform.org/gist/5259299)

An example of how a positive spread distance length value affects the drop shadow. If a spread distance is defined, the shadow is expanded outward or contracted inward.

``` css
article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 5px 10px rgba(0, 0, 0, 0.5);
}
```

[View live example](http://code.webplatform.org/gist/5259449)

Negative values cause the shadow shape to contract.

``` css
article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 20px 5px -10px rgba(0, 0, 0, 0.5);
}
```

[View live example](http://code.webplatform.org/gist/5259463)

If the blur value is zero, the shadow's edge is sharp. (A non-zero blur value indicates the resulting shadow should be blurred, such as by a Gaussian filter.)

``` css
article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 0 5px rgba(0, 0, 0, 0.5);
}
```

[View live example](http://code.webplatform.org/gist/5259501)

If the box has a nonzero ‘border-radius’, the shadow shape is rounded in the same way. (The ‘border-image’ does not affect the shape of the box-shadow.)

``` css
article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 1);
   border-radius: 10px;
}
```

[View live example](http://code.webplatform.org/gist/5259470)

An example of a multiple box-shadows. The inner shadow appears on all four sides by creating two box-shadows.

``` html
<style>
    .shadow-style {
        width: 100px;
        height: 100px;
        box-shadow: inset 30px 30px 5px green, inset -30px -30px 5px blue;
        border: 10px solid yellow;
        background-color: red;
    }
</style>
<body>
    <div class="shadow-style">
    </div>
</body>
```

[View live example](http://code.webplatform.org/gist/5259531)

## <span>Usage</span>

     ===Remarks===

See also:

-   [css/data\_types/length](/css/data_types/length)
-   [css/color](/css/color)

## <span>Related specifications</span>

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#box-shadow)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   **box-shadow**

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

#### <span>Box Model</span>

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   **box-shadow**

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)
