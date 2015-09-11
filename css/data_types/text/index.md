---
title: Text values in CSS properties
readiness: 'Ready to Use'
summary: 'Various CSS data types are expressed using character text, however the meaning and syntax of each type differs.'
tags:
  - Concept
  - Pages
  - CSS
uri: 'css/data types/text'

---
## <span>Summary</span>

Various CSS data types are expressed using character text, however the meaning and syntax of each type differs.

 Text-like [CSS data-types](/css/data_types) include:

-   [`<string>`s](/css/data_types/string)

-   [`<custom-ident>` (custom identifier) values](/css/data_types/custom_ident)

-   [keywords](/css/data_types/keyword)

In addition, various [CSS functions](/css/functions) can be used to generate values of these or other data types.

## <span>Examples</span>

``` css
a[href$=".pdf"]::after {
    /* literal string marks links to PDF files */
    content: " (PDF)";
}
```

``` css
.pulse {
    /* identifier for keyframe animation defined below */
    animation-name: pulse
    animation-duration: 1s;
    /* property values are built-in keywords */
    animation-direction: alternate;
    animation-iteration-count: infinite;
    /* The url() function accepts a string value */
    background-image: url(img/icon.png);
}

/* "pulse" is referenced above by animation-name property */
@keyframes pulse {
    from { opacity: 1   }
    to   { opacity: 0.5 }
}
```

## <span>Related specifications</span>

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation
