---
title: outline-offset
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-offset property offsets the outline and draw it beyond the border edge.'
code_samples:
  - 'http://gist.github.com/5579301'
uri: css/properties/outline-offset

---
# outline-offset

## Summary

The outline-offset property offsets the outline and draw it beyond the border edge.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   \<length\> value in absolute units (px or physical).
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `outlineOffset`
Percentages
:   N/A

## Syntax

-   `outline-offset: <length>`
-   `outline-offset: inherit`

## Values

\<length\>
:   Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length).�

inherit
:   This is a keyword indicating that the value is inherited from their parent's element calculated value.

## Examples

A simple example showing multiple \<span\>s with border and outline.

``` {.html}
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
</div>
```

[View live example](http://code.webplatform.org/gist/5579301)

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
  border: red solid 3px;
  outline: blue solid 3px;
}

.all .one {
  outline-offset: 0px;
}

.all .two {
  outline-offset: 5px;
}

.all .three {
  outline-offset: 0.2em;
}
```

[View live example](http://code.webplatform.org/gist/5579301)

## Usage

     If the computed value of ‘outline-offset’ is anything other than 0, then the outline is outset from the border edge by that amount.

## Related specifications

Specification
:   Status
[CSS Basic User Interface Module Level 3 (CSS3 UI)](http://dev.w3.org/csswg/css-ui/#outline-offset0)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

