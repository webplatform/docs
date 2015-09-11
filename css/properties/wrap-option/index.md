---
title: wrap-option
notes:
  - 'Obsolete; not in current W3C spec.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`wrap`'
  'Applies to': 'all elements and generated content'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Not Ready'
summary: "Obsolete and unsupported. Do not use.\n"
tags:
  - CSS
  - Properties
uri: css/properties/wrap-option

---
## <span>wrap-option (Obsolete)</span>

For technical reasons, the title of this article is not the text used to call this API. Instead, use `wrap-option (Obsolete)`

## <span>Summary</span>

Obsolete and unsupported. Do not use.

This CSS property controls the text when it reaches the end of the block in which it is enclosed.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `wrap`

Applies to
:   all elements and generated content

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `wrap-option: emergency`
-   `wrap-option: no-wrap`
-   `wrap-option: soft-wrap`
-   `wrap-option: wrap`

## <span>Values</span>

wrap
:   The text is wrapped at the best line-breaking opportunity (if required) within the available block inline-progression dimension

no-wrap
:   The text is only wrapped where explicitly specified by preserved line feed characters. In the case when lines are longer than the available block width, the overflow will be treated in accordance with the 'overflow' property specified in the element.

soft-wrap
:   The text is wrapped after the last character which can fit before the ending-edge of the line and where explicitly specified by preserved line feed characters. No line-breaking algorithm is invoked. The intended usage is the rendering of a character terminal emulation.

emergency
:   The text is wrapped like for the 'wrap' case, except that the line-breaking algorithm will allow as a last resort option a text wrap after the last character which can fit before the ending edge of the line box, independently of 'line-break', 'word-break-cjk' and 'word-break-inside' properties. For example, this addresses the situation of very long words constrained in a fixed-width container with no scrolling allowed.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Could not find any documentation that this is still relevant, concur that it should be deleted.

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514)
:   Obsolete (previously a Candidate Recommendation)

## <span>See also</span>

### <span>Other articles</span>

See also: [wrap-flow](/css/properties/wrap-flow) property