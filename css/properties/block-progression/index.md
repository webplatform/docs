---
title: block-progression
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`tb`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: 'Sets the block progression and layout orientation: deprecated in favor of the writing-mode property.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/block-progression

---
## Summary

Sets the block progression and layout orientation: deprecated in favor of the writing-mode property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `tb`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `block-progression: bt`
-   `block-progression: lr`
-   `block-progression: rl`
-   `block-progression: tb`

## Values

tb
:   Default. Top-to-bottom block flow. Layout is horizontal.

rl
:   Right-to-left block flow. Layout is vertical.

bt
:   Bottom-to-top block flow. Layout is horizontal.

lr
:   Left-to-right block flow. Layout is vertical.

**Needs Examples**: This section should include examples.

## Usage

     ===Deprecated===

This property has been dropped from the current version of [CSS Writing Modes specification](http://dev.w3.org/csswg/css-writing-modes=the). You are encouraged to manipulate an element's writing mode via the [**writing-mode**](/css/properties/writing-mode) property instead.

## Notes

### Remarks

In vertical layout, text lines are rotated 90° clockwise. Images are not rotated, but tables are. Box layout in vertical orientations is exactly analogous to layout in the horizontal orientation: width, height, top, bottom, right, and left do not rotate with the text. Only one block progression is active at a time; these values cannot be combined. See [**-ms-writing-mode**](/css/properties/writing-mode) for additive block progression values. This property is based on the block-progression property of the [CSS3 Text Layout](http://go.microsoft.com/fwlink/p/?linkid=203505) module.

### Syntax

`-ms-block-progression: tb | rl | bt | lr`

### Standards information

There are no standards that apply here.

## Related specifications

[CSS Text Level 3](http://www.w3.org/TR/2003/CR-css3-text-20030514/#block-progression)
:   [Obsolete] W3C Candidate Recommendation

[CSS Writing Mode Level 3](http://www.w3.org/TR/css3-writing-modes/)
:   W3C Working Draft

## See also

### Related articles

#### Text

-   **block-progression**

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `direction`
