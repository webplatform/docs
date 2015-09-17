---
title: 'CSS keywords'
code_samples:
  - 'http://gist.github.com/10615256'
readiness: 'Ready to Use'
standardization_status: Mixed
summary: 'Many CSS properties have specific keywords which may be used as values; in addition, the keywords initial and inherit may be used as the value of any CSS property.'
tags:
  - Data_Type
  - CSS
uri: 'css/data types/keyword'

---
## Summary

Many CSS properties have specific keywords which may be used as values; in addition, the keywords initial and inherit may be used as the value of any CSS property.

 The keywords relevant to a specific CSS property are defined in its [property page](/css/properties). All keywords meet the requirements of [CSS identifiers](/css/data_types/custom_ident), and are case sensitive. Keywords should never be quoted.

### CSS-wide keywords

Certain keywords can be used for any CSS property value:

-   **inherit** copies the value of the property in effect for the element's parent.

-   **initial** represents the initial (or default) value for the property, over-riding any values set earlier in the cascade; initial values are defined on each property's definition; it is not supported in Internet Explorer.

-   **unset** is equivalent to **inherit** if the property is normally inherited, or **initial** otherwise; it is not currently supported in most browsers (although Firefox implements it).

## Examples

``` css
body{
    height:100%;
    background-image:radial-gradient(ellipse , yellow, orange 30%);
    text-align:center;
    /* a property-specific keyword */
}
h1 {
   background-image:inherit;
   /* inherit a not-normally inherited property
      (note that there is a second gradient that fits the
      heading box)
   */
}
p {
   text-align:initial;
   /* over-ride an inheritied property,
      if your browser supports the initial keyword */
}
a {
  color: inherit !important;
  /* over-ride a user stylesheet property */

  text-decoration: unset !important;
  /* over-ride a user stylesheet property,
     if your browser supports the unset keyword */
}
```

[View live example](http://gist.github.com/10615256)

## Related specifications

[CSS Cascading and Inheritance Level 3](http://www.w3.org/TR/css3-cascade/#inherit-initial)
:   W3C Candidate Recommendation

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#keywords)
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/cascade.html#value-def-inherit)
:   W3C Recommendation
