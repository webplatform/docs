---
title: appearance
tags:
  0: CSS
  1: Properties
  3: Design
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Add example, description, compatibility.'
summary: 'Allows changing the style of any element to platform-based interface elements or vice versa.'
uri: css/properties/appearance

---
# appearance

## Summary

Allows changing the style of any element to platform-based interface elements or vice versa.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   all elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specific value
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   N/A

## Syntax

-   `appearance: button`
-   `appearance: button-arrow-down`
-   `appearance: button-arrow-next`
-   `appearance: button-arrow-previous`
-   `appearance: button-arrow-up`
-   `appearance: button-bevel`
-   `appearance: button-focus`
-   `appearance: caret`
-   `appearance: checkbox`
-   `appearance: checkbox-container`
-   `appearance: checkbox-small`
-   `appearance: dialog`
-   `appearance: listbox`
-   `appearance: none`

## Values

button-arrow-down
:   Firefox specific - but no effect in latest version

button-arrow-next
:   Firefox specific - but no effect in latest version

button-arrow-previous
:   Firefox specific - but no effect in latest version

button-arrow-up
:   Firefox specific - but no effect in latest version

button-focus
:   Firefox specific - but no effect in latest version

caret
:   No clear visual effect.

none
:   No special styling is applied. For Firefox note [bug 649849](https://bugzilla.mozilla.org/show_bug.cgi?id=649849) and [bug 605985](https://bugzilla.mozilla.org/show_bug.cgi?id=605985)

button
:   The element is drawn like a button

button-bevel
:   Use button bevel theme for rendering the object. Seems to work only in mozilla based browsers

checkbox
:   The element is drawn like a checkbox, including only the actual "checkbox" portion.

checkbox-container
:   Firefox specific - but no effect in latest version

checkbox-small
:   Firefox specific - but no effect in latest version

dialog
:

listbox
:

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[CSS3 Basic User Interface Module](http://www.w3.org/TR/2004/CR-css3-ui-20040511/#appearance)
:   W3C Candidate Recommendation (Obsolete)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/-moz-appearance?redirectlocale=en-US&redirectslug=CSS%3A-moz-appearance)

}}