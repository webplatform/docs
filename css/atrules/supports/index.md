---
title: '@supports'
code_samples:
  - 'http://dabblet.com/gist/3895764'
compatibility:
  feature: '@supports'
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The CSS @supports at-rule lets authors detect support of CSS features directly in CSS.'
tags:
  - CSS_At_Rules
  - CSS
uri: css/atrules/@supports

---
## Summary

The CSS @supports at-rule lets authors detect support of CSS features directly in CSS.

 The CSS at-rule `@supports` is part of the [CSS Conditional Rules Module Level 3](http://dev.w3.org/csswg/css3-conditional/) Draft. It allows authors to condition rules based on whether particular property declarations are supported in CSS.

In other words `@supports` lets you detect browser support of CSS features directly in CSS. [Modernizr](http://modernizr.com/) is a well known library that detects features using JavaScript.

The operators `and` and `or` allows to chain the detection of several features.

## Examples

An abstract example with the detection of support for `display: flex` (known as [CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/)):

``` css
@supports (display: flex) {
  div {
    display: flex;
  }
}
```

Chaining detection of several features using the operator `and`:

``` css
@supports (background: rgba(0,0,0,0.2)) and (opacity: 0.8) {
  body {
    background: rgba(0,0,0,0.2);
  }

  div {
    opacity: 0.8;
  }
}
```

To detect if an experimental feature is supported with vendor-prefixes the `or` operator might be helpful:

(This example does not include `-o-` and `-ms-` prefixes as neither Opera nor Microsoft supported a prefixed version of `box-shadow`.)

``` css
@supports (-webkit-box-shadow: 0 0 2px #000) or
          (   -moz-box-shadow: 0 0 2px #000) or
          (        box-shadow: 0 0 2px #000) {

  div {
    -webkit-box-shadow: 0 0 2px #000;
       -moz-box-shadow: 0 0 2px #000;
            box-shadow: 0 0 2px #000;
  }
}
```

## Usage

     Browser support for this feature is still pretty limited.

## Related specifications

[CSS Conditional Rules Module Level 3](http://www.w3.org/TR/css3-conditional/)
:   Candidate Recommendation

## See also

### Related articles

#### Syntax

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   **@supports**

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)

### External resources

-   [@supports in the CSS Conditional Rules Editor's Draft](http://dev.w3.org/csswg/css3-conditional/#at-supports)
-   [@supports in the MDN](https://developer.mozilla.org/en-US/docs/CSS/@supports)
-   [Test-case](http://dabblet.com/gist/3895764)
-   [On Firefox' support in version 17](http://mcc.id.au/blog/2012/08/supports)
-   [Support in Opera 12.1](http://my.opera.com/desktopteam/blog/2012/10/09/flexbox-and-supports)
