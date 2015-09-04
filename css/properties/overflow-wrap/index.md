---
title: overflow-wrap
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property specifies whether or not particularly long words will be ''broken'' (separated into multiple lines) if necessary in order to fit in within its container.'
code_samples:
  - 'http://gist.github.com/5842405'
uri: css/properties/overflow-wrap

---
# overflow-wrap

## Summary

This property specifies whether or not particularly long words will be 'broken' (separated into multiple lines) if necessary in order to fit in within its container.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`
Applies to
:   all elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specified value
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `overflowWrap`
Percentages
:   N/A

## Syntax

-   `overflow-wrap: break-word`
-   `overflow-wrap: normal`

## Values

normal
:   Lines can only be broken at normal break points (spaces, non-alphanumeric characters, etc.)

This is the default option.

break-word
:   Lines can be broken at any point if necessary to preserve the limits of the container element -- for example, "hamburger" can be broken into "ham" and "burger" across separate lines.

## Examples

We can compare two identical blocks of texts and see how the two possible values of **overflow-wrap** change the display of lines which do not fit within the container.

``` {.css}
/* Using the CSS 'overflow-wrap' property. */
p {
    width: 5em;
    float: left;
    margin-right: 3em;
}

p:nth-child(1) {
    overflow-wrap: normal;
}

p:nth-child(2) {
    overflow-wrap: break-word;
}
```

[View live example](http://code.webplatform.org/gist/5842405)

## Usage

     This property is only in use when white-space allows wrapping.

## Notes

[**word-wrap**](/css/properties/word-wrap) is a commonly used alias for **overflow-wrap**; specifically, **word-wrap** was a prior iteration of the property. Most browsers recognize **word-wrap**, but usage of **overflow-wrap** should be encouraged.

## Related specifications

Specification
:   Status
[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#overflow-wrap-property)
:   Last Call Working Draft

