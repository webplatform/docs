---
title: all-space-treatment
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`collapse`'
  'Applies to': 'All elements and generated content.'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: ''
  '[Computed value](/css/concepts/computed_value)': 'As specified (except for initial and inherit).'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the treatment of all consecutive white space characters (with no exception for line feed characters).'
tags:
  - CSS
  - Properties
uri: css/properties/all-space-treatment

---
## <span>Summary</span>

Specifies the treatment of all consecutive white space characters (with no exception for line feed characters).

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `collapse`

Applies to
:   All elements and generated content.

[Inherited](/css/concepts/inherited)
:   Yes

Media
:

[Computed value](/css/concepts/computed_value)
:   As specified (except for initial and inherit).

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `all-space-treatment: collapse`
-   `all-space-treatment: preserve`

## <span>Values</span>

collapse
:   The white space characters are collapsed according to the rules described in [white space processing](http://www.w3.org/TR/2003/CR-css3-text-20030514/#white-space-processing).

preserve
:   All white space characters are rendered as they are.

## <span>Examples</span>

``` css
/* preserve */
p.asis {
    all-space-treatment: preserve;
}
```

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514)
:   W3C Candidate Recommendation
