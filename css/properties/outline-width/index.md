---
title: outline-width
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-width property sets the width of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.'
code_samples:
  - 'http://gist.github.com/5579241'
uri: css/properties/outline-width

---
# outline-width

## Summary

The outline-width property sets the width of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `medium`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   absolute length; ‘0’ if the outline style is ‘none’.
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `outlineWidth`
Percentages
:   N/A

## Syntax

-   `outline-width: <width>`
-   `outline-width: inherit`
-   `outline-width: medium`
-   `outline-width: thick`
-   `outline-width: thin`

## Values

medium
:   Default. �

thin
:   Less than the default width.

thick
:   Greater than the default width.

\<width\>
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

inherit
:   This is a keyword indicating that the value is inherited from their parent's element calculated value.

## Examples

A simple example showing multiple \<span\>s.

``` {.html}
<div class="all">
    <p>
      <span class="medium">Medium</span>
    </p>
    <p>
      <span class="thin">Thin</span>
    </p>
    <p>
      <span class="thick">Thick</span>
    </p>
    <p>
      <span class="width">10px</span>
    </p>
</div>
```

[View live example](http://code.webplatform.org/gist/5579241)

CSS outline width values.

``` {.css}
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
  outline-style: solid;
}

.all .medium {
  outline-width: medium;
}

.all .thin {
  outline-width: thin;
}

.all .thick {
  outline-width: thick;
}

.all .width {
  outline-width: 10px;
}
```

[View live example](http://code.webplatform.org/gist/5579241)

## Notes

-   Displaying an outline does not cause reflow, no matter how wide the outline is. The outline frame is drawn over an element, and does not influence the position or size of the box, or of any other boxes.
-   The [outline](/css/properties/outline) property is a shorthand property for setting one or more of the individual outline properties [outline-style](/css/properties/outline-style), **outline-width** and [outline-color](/css/properties/outline-color) in a single rule. In most cases the use of this shortcut is preferable and more convenient.

## Related specifications

Specification
:   Status
[CSS Basic User Interface Module Level 3 (CSS3 UI)](http://dev.w3.org/csswg/css-ui/#outline-width0)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

