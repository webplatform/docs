---
title: background-blend-mode
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: "This property describes how the element's background images should blend with each other and the element's background color. \nThe value is a list of blend modes that corresponds to each background image. Each element in the list will apply to the corresponding element of background-image. If a property doesn’t have enough comma-separated values to match the number of layers, the UA must calculate its used value by repeating the list of values until there are enough.\n"
code_samples:
  - 'http://gist.github.com/10908092'
uri: css/properties/background-blend-mode

---
# background-blend-mode

## Summary

This property describes how the element's background images should blend with each other and the element's background color. The value is a list of blend modes that corresponds to each background image. Each element in the list will apply to the corresponding element of background-image. If a property doesn’t have enough comma-separated values to match the number of layers, the UA must calculate its used value by repeating the list of values until there are enough.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `<normal>#`
Applies to
:   All HTML and SVG elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   No

## Syntax

-   `background-blend-mode: color`
-   `background-blend-mode: color-burn`
-   `background-blend-mode: color-dodge`
-   `background-blend-mode: darken`
-   `background-blend-mode: difference`
-   `background-blend-mode: exclusion`
-   `background-blend-mode: hard-light`
-   `background-blend-mode: hue`
-   `background-blend-mode: lighten`
-   `background-blend-mode: luminosity`
-   `background-blend-mode: multiply`
-   `background-blend-mode: normal`
-   `background-blend-mode: overlay`
-   `background-blend-mode: saturation`
-   `background-blend-mode: screen`
-   `background-blend-mode: soft-light`

## Values

normal
:   This is the default attribute which specifies no blending. The blending formula simply selects the source color.

multiply
:   The source color is multiplied by the destination color and replaces the destination. The resultant color is always at least as dark as either the source or destination color. Multiplying any color with black results in black. Multiplying any color with white preserves the original color.

screen
:   Multiplies the complements of the backdrop and source color values, then complements the result. The result color is always at least as light as either of the two constituent colors. Screening any color with white produces white; screening with black leaves the original color unchanged. The effect is similar to projecting multiple photographic slides simultaneously onto a single screen.

overlay
:   Multiplies or screens the colors, depending on the backdrop color value. Source colors overlay the backdrop while preserving its highlights and shadows. The backdrop color is not replaced but is mixed with the source color to reflect the lightness or darkness of the backdrop.

darken
:   The backdrop is replaced with the source where the source is darker; otherwise, it is left unchanged.

lighten
:   Selects the lighter of the backdrop and source colors. The backdrop is replaced with the source where the source is lighter; otherwise, it is left unchanged.

color-dodge
:   Brightens the backdrop color to reflect the source color. Painting with black produces no changes.

color-burn
:   Darkens the backdrop color to reflect the source color. Painting with white produces no change.

hard-light
:   Multiplies or screens the colors, depending on the source color value. The effect is similar to shining a harsh spotlight on the backdrop.

soft-light
:   Darkens or lightens the colors, depending on the source color value. The effect is similar to shining a diffused spotlight on the backdrop.

difference
:   Subtracts the darker of the two constituent colors from the lighter color. Painting with white inverts the backdrop color; painting with black produces no change.

exclusion
:   Produces an effect similar to that of the Difference mode but lower in contrast. Painting with white inverts the backdrop color; painting with black produces no change.

hue
:   Creates a color with the hue of the source color and the saturation and luminosity of the backdrop color.

saturation
:   Creates a color with the saturation of the source color and the hue and luminosity of the backdrop color. Painting with this mode in an area of the backdrop that is a pure gray (no saturation) produces no change.

color
:   Creates a color with the hue and saturation of the source color and the luminosity of the backdrop color. This preserves the gray levels of the backdrop and is useful for coloring monochrome images or tinting color images.

luminosity
:   Creates a color with the luminosity of the source color and the hue and saturation of the backdrop color. This produces an inverse effect to that of the Color mode.

## Examples

A group of boxes that show different blend effects.

``` {.html}
<div class='normal'>      <label>Normal</label>       </div>
<div class='multiply'>        <label>Multiply</label>     </div>
<div class='screen'>      <label>Screen</label>       </div>
<div class='overlay'>     <label>Overlay</label>      </div>
<div class='darken'>      <label>Darken</label>       </div>
<div class='ligthen'>     <label>Ligthen</label>      </div>
<div class='color-dodge'> <label>Color-dodge</label>  </div>
<div class='color-burn'>  <label>Color-burn</label>   </div>
<div class='hard-light'>  <label>Hard-light</label>   </div>
<div class='soft-light'>  <label>Soft-light</label>   </div>
<div class='difference'>  <label>Difference</label>   </div>
<div class='exclusion'>       <label>Exclusion</label>    </div>
<div class='hue'>         <label>Hue</label>          </div>
<div class='saturation'>  <label>Saturation</label>   </div>
<div class='color'>           <label>Color</label>        </div>
<div class='luminosity'>  <label>Luminosity</label>   </div>
```

[View live example](http://code.webplatform.org/gist/10908092)

``` {.css}
body {
    margin: 2em;
}

div {
/*  In the background of the element it's necessary to have two backgrounds (image, gradient, color)
    background: first-background properties, second-background properties; */
    background: url(imageA.png) no-repeat center, url(imageB.png) no-repeat center;
    border-radius: 10px;
    box-shadow: 5px 2px 10px #888;
    display: inline-block;
    height:200px;
    margin: 1em;
    opacity: 0.5;
    transition: opacity .25s ease-in-out;
    width: 200px;
}

label {
    display:block;
    background: #fff;
    font-family: Georgia, Garamond, serif;
    text-align:center;
    text-shadow: .5px .7px .7px #eee;
}

div:hover { opacity: 1.0; }

// background-blend-mode: blend-mode;
.normal      { background-blend-mode: normal;      }
.multiply    { background-blend-mode: multiply;    }
.screen      { background-blend-mode: screen;      }
.overlay     { background-blend-mode: overlay;     }
.darken      { background-blend-mode: darken;      }
.ligthen     { background-blend-mode: ligthen;     }
.color-dodge { background-blend-mode: color-dodge; }
.color-burn  { background-blend-mode: color-burn;  }
.hard-light  { background-blend-mode: hard-light;  }
.soft-light  { background-blend-mode: soft-light;  }
.difference  { background-blend-mode: difference;  }
.exclusion   { background-blend-mode: exclusion;   }
.hue         { background-blend-mode: hue;         }
.saturation  { background-blend-mode: saturation;  }
.color       { background-blend-mode: color;       }
.luminosity  { background-blend-mode: luminosity;  }
```

## Usage

     The ‘background-blend-mode’ list must be applied in the same order as ‘background-image’. This means that the first element in the list will apply to the layer that is on top. If a property doesn't have enough comma-separated values to match the number of layers, the UA must calculate its used value by repeating the list of values until there are enough.

If the ‘background’ shorthand is used, the ‘background-blend-mode’ property for that element must be reset to its initial value.

## Notes

**Separable blend modes** *(normal, multiply, screen, overlay, darken, lighten, color-dodge, color-burn, hard-light, soft-light, difference, exclusion)*

A blend mode is termed separable if each component of the result color is completely determined by the corresponding components of the constituent backdrop and source colors — that is, if the mixing formula is applied separately to each set of corresponding components.

**Non-separable blend modes** *(hue, saturation, color, luminosity)*

Non-separable blend modes consider all color components in combination as opposed to the seperable ones that look at each component individually.

## Related specifications

Specification
:   Status
[Compositing and Blending Level 1](http://www.w3.org/TR/compositing/#blending)
:   Candidate recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   **background-blend-mode**

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### CSS Attributes

-   **background-blend-mode**

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

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

#### Visual Effects

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   **background-blend-mode**

-   [clip](/css/properties/clip)

-   [cursor](/css/properties/cursor)

-   [opacity](/css/properties/opacity)

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

-   [Introducing CSS blending](http://www.adobe.com/devnet/html5/articles/css-blending.html) by Rik Cabanier
-   [[1]](http://blogs.adobe.com/webplatform/2014/06/12/background-blending-now-available-in-firefox-30/) by Rik Cabanier
-   [[2]](http://codepen.io/collection/Hcdol/) by Adobe
-   [[3]](http://bennettfeely.com/gradients/) by Bennett Feely
-   [[4]](http://codepen.io/collection/fEkjb/) by yoksl

