---
title: 'var'
code_samples:
  - 'http://gist.github.com/a41474c974dfef4ec106'
compatibility:
  feature: var
  topic: css
notes:
  - 'Add values/parameters, syntax, example, compatibility.'
readiness: 'Not Ready'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Allows authors to reference the value of a custom property for cascading variables.'
tags:
  - CSS_Functions
  - CSS
uri: css/functions/var

---
## Summary

Allows authors to reference the value of a custom property for cascading variables.

## Syntax

-   **var ( \<custom-property\> )**
-   **var ( \<custom-property\>, \<default-value\> )**

## Parameters

**custom-property**

*The name of the custom property to use.*

**default-value**

*A value to use when the custom property isn't defined.*

## Examples

``` css
.block .header {
    /* use a variable for the text color of the header, with default 'blue' */
    color: var(--header-color, blue);

    /* use a variable for the background color of the header, with default 'blue' */
    background-color: var(--text-color, blue);

    padding: 1em;
}

.block .contents{
    /* use a variable for the text color of the contents, with default 'red' */
    color: var(--text-color, red);
    padding: 1em;
}

.block{
    /* only the --text-color variable is set, so the --header-color will show it's default 'blue' */
    --text-color: green;
}
```

[View live example](http://gist.github.com/a41474c974dfef4ec106)

## Related specifications

[CSS Custom Properties for Cascading Variables Module Level 1](http://www.w3.org/TR/css-variables-1/)
:   W3C Last Call Working Draft
