---
title: 'outline-style'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5579124'
compatibility:
  feature: outline-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`outlineStyle`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-style property sets the style of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/outline-style

---
## Summary

The outline-style property sets the style of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `outlineStyle`

Percentages
:   N/A

## Syntax

-   `outline-style: auto`
-   `outline-style: dashed`
-   `outline-style: dotted`
-   `outline-style: double`
-   `outline-style: groove`
-   `outline-style: inherit`
-   `outline-style: inset`
-   `outline-style: none`
-   `outline-style: outset`
-   `outline-style: ridge`
-   `outline-style: solid`

## Values

none
:   Default. Outline is not drawn, color and width are ignored.

dotted
:   A series of round or square dots.

dashed
:   A series of square-ended dashes.

solid
:   A single line segment.

double
:   Outline is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [outline-width](/css/properties/outline-width) value. The border width must be at least 3 pixels wide to draw a double outline.

groove
:   Looks as if it were carved in the canvas. (This is typically achieved by creating a “shadow” from two colors that are slightly lighter and darker than the [outline-color](/css/properties/outline-color).)

ridge
:   Looks as if it were coming out of the canvas.

inset
:   Looks as if the content on the inside of the outline is sunken into the canvas.

outset
:   Looks as if the content on the inside of the outline is coming out of the canvas.

inherit
:   This is a keyword indicating that the value is inherited from their parent's element calculated value.

auto
:   Defined by the user agent (browser). Currently supported only in WebKit. This value allows user-agents to draw focus outlines on elements in an appropriate platform-native style, or in some other appropriate style if there is no platform-native style.

## Examples

A simple example showing multiple \<span\>s.

``` html
<div class="all">
<p>
      <span class="one">One</span>
    </p>
    <p>
      <span class="two">Two</span>
    </p>
    <p>
      <span class="three">Three</span>
    </p>
    <p>
      <span class="four">Four</span>
    </p>
    <p>
      <span class="five">Five</span>
    </p>
    <p>
      <span class="six">Six</span>
    </p>
    <p>
      <span class="seven">Seven</span>
    </p>
    <p>
      <span class="eight">Eight</span>
    </p>
    <p>
      <span class="nine">Nine</span>
    </p>
</div>
```

[View live example](http://gist.github.com/5579124)

Outline styles in CSS.

``` css
.all {
  background-color: lightgrey;
}

.all p {
  padding: 20px;
}

.all span {
  padding: 10px;
  margin: 10px 10px 10px 10px;
  font-size: 36px;
  font-family: Bitter;
  outline-width: 5px;
}

.all .one {
  outline-style: none;
}

.all .two {
  outline-style: outset;
}

.all .three {
  outline-style: dotted;
}

.all .four {
  outline-style: dashed;
}

.all .five {
  outline-style: solid;
}

.all .six {
  outline-style: double;
}

.all .seven {
  outline-style: groove;
}

.all .eight {
  outline-style: ridge;
}

.all .nine {
  outline-style: inset;
}
```

[View live example](http://gist.github.com/5579124)

## Notes

-   This property accepts the same values as [border-style](/css/properties/border-style), ***except*** that ‘hidden’ is not a legal outline style.
-   The [outline](/css/properties/outline) property is a shorthand property for setting one or more of the individual outline properties **outline-style**, [outline-width](/css/properties/outline-width) and [outline-color](/css/properties/outline-color) in a single rule. In most cases the use of this shortcut is preferable and more convenient.

## Related specifications

[CSS Basic User Interface Module Level 3 (CSS3 UI)](http://dev.w3.org/csswg/css-ui/#outline-style0)
:   Working Draft
