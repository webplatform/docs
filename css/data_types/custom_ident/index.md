---
title: <custom-ident>
code_samples:
  - 'http://gist.github.com/10605942'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The &lt;custom-ident&gt; CSS data type represents an identifier token created by the stylesheet author to reference content in a different part of the stylesheet.  It is used for counters and for animation.'
tags:
  - Data
  - Type
  - CSS
uri: 'css/data types/custom ident'

---
## Summary

The &lt;custom-ident&gt; CSS data type represents an identifier token created by the stylesheet author to reference content in a different part of the stylesheet. It is used for counters and for animation.

 Identifiers are case-sensitive. Valid custom identifier values:

-   should usually contain letters, digits, non-ASCII characters, or the underscore (**\_**) or hyphen (**-**) characters;
-   *may* contain other ASCII characters if escaped with backslash (**\\**);
-   must not use a digit as the first character unless it is escaped;
-   must not match any keywords that are valid values for the property where it is used;
-   must not match the CSS-wide keywords "initial" or "inherit" or the reserved word "default", in any combination of upper or lowercase letters.

Identifiers are not quoted.

## Examples

The example uses three custom identifiers: `h1-counter`, `subSectionCounter`, and `colorChange`.

``` css
h1 {
    counter-increment: h1-counter;
    counter-reset: subSectionCounter;
    animation: colorChange 3s infinite alternate;
}
h1::before {
    content: counter(h1-counter);
      /*counter tokens can contain digits and hyphens */
   padding:0.5em;
}
h2 {
   counter-increment: subSectionCounter; /* note case must match exactly */
}
h2::before {
   content: counter(h1-counter)  "."  counter(subSectionCounter);
   padding:0.5em;
}
@keyframes colorChange {
   from {
     color:blue;
   }
   to {
     color:green;
   }
}
```

[View live example](http://code.webplatform.org/gist/10605942)

## Related specifications

<http://www.w3.org/TR/css3-values/#custom-idents>
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#counter)
:   W3C Recommendation
