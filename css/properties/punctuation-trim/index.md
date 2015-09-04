---
title: punctuation-trim
tags:
  - CSS
  - Properties
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Obsolete; deletion candidate'
summary: "Obsolete: unsupported.\n"
uri: css/properties/punctuation-trim

---
# punctuation-trim

## Summary

Obsolete: unsupported.

This property determines whether or not a full-width punctuation mark character should be trimmed if it appears at the beginning of a line, so that its "ink" lines up with the first glyph in the line above and below.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   block-level and inline-block elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``

## Syntax

-   `punctuation-trim: none`
-   `punctuation-trim: start`

## Values

none
:   Leading punctuation is not trimmed.

start
:   Leading punctuation is trimmed.

## Usage

     Use this property to trim the leading whitespace of a punctuation glyph when it is the first character on a line. Please see the images in the spec, which shows in a concise way what will happen.

## Related specifications

Specification
:   Status
[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#punctuation-trim)
:   Obsolete (previously Candidate Recommendation)

