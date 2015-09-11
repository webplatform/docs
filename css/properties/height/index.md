---
title: height
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5702862'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'percentage or absolute height'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the height of an element. The content area of the element height does not include the padding, border, and margin of the element.'
tags:
  - CSS
  - Properties
uri: css/properties/height

---
## <span>Summary</span>

Sets the height of an element. The content area of the element height does not include the padding, border, and margin of the element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   percentage or absolute height

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `height: auto`
-   `height: available`
-   `height: border-box`
-   `height: content-box`
-   `height: fit-content`
-   `height: height`
-   `height: max-content`
-   `height: min-content`
-   `height: percentage`

## <span>Values</span>

auto
:   If auto is set for the elements height, the browser will determine the height for the element.

height
:   Will take a number that is immediately followed by a length unit such as px, em, in, etc.

percentage
:   Integer followed by a percent sign (%). The value is a percentage of the height of the parent object, which must be specified explicitly. Negative values are not allowed.

border-box
:   If border-box is used, the height or percentage defined will be applied to the element's border box.

content-box
:   If content-box is used, the height or percentage defined will be applied to the element's content-box.

max-content
:   The intrinsic preferred height

min-content
:   The intrinsic minimum height

available
:   The containing block height minus horizontal margin, border, and padding

fit-content
:   This will be either the large of the minimum height or the smaller of the preferred height and the available height

## <span>Examples</span>

``` css
/* Height of div equal to 100% of the bounding element */
div { height: 100% }

/* Height of h1 equal to 20em */
h1 { height: 20em }

/* Height set to auto */
section { height: auto }

/* Height of image set to 100px */
img { height: 100px }
```

Example using new values that are part of the CSS Basic Box Model that is currently in working draft.

``` html
<style>
/**
 * Height values of the CSS Box Model working draft
 */

div {
    box-sizing: border-box;
    border: 1px solid #444;
    margin: 5px;
    width: 250px;
}

p {
    background: #000;
    color: lightgrey;
    padding: 5px;
    font-family: Arial, sans-serif;
}

p.height200 {
    /* vendor prefix needed */
    height: 200px;
    background: blue;
    color: orange;
}

p.height50 {
    /* vendor prefix needed */
    height: 50px;
    background: red;
}

p.height50solved {
    /* vendor prefix needed */
    height: 50px;
    background: green;
    overflow: hidden;
}
</style>
<div>
<p>This is the content inside of the parent div. Height is not set, so the height is defaulting to auto.</p>
</div>

<div>
<p class="height200">This is the content inside of the parent div. It's height is set to 200px</p>
</div>

<!-- You can solve the issue below by setting the overflow property -->
<div>
<p class="height50">This is the content inside of the parent div. The content extends beyond the bounding element and extends into elements below, interupting the flow.</p>
</div>

<!-- Solved by setting the overflow property to hidden -->
<div>
<p class="height50solved">This is the content inside of the parent div. The content extends beyond the bounding element and extends into elements below, interupting the flow.</p>
</div>
```

[View live example](http://code.webplatform.org/gist/5702862)

## <span>Notes</span>

### <span>Remarks</span>

If you specify the **height** property of an **img** object but not the [**width**](/css/properties/width) property, the width is proportional to the height according to the dimensions of the image source file. To perform operations on the numeric value of this property, use [**pixelHeight**](/css/cssom/properties/pixelHeight) or [**posHeight**](/css/cssom/properties/posHeight).

## <span>Related specifications</span>

[CSS Basic Box Model](http://dev.w3.org/csswg/css-box/#the-width-and-height-properties)
:   Working Draft

[CSS Level 2](http://www.w3.org/TR/CSS2/visudet.html#the-height-property)
:   Recommendation

[CSS Level 1](http://www.w3.org/TR/CSS1/#height)
:   Recommendation

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

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   **height**

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### <span>Box Model</span>

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   **height**

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

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   **height**

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### <span>Grid Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-column-position](/css/properties/grid-column-position)

-   [grid-column-span](/css/properties/grid-column-span)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [grid-row-position](/css/properties/grid-row-position)

-   **height**

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `Conceptual`
-   `Measuring Element Dimension and Location with CSSOM in Internet Explorer 9`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
