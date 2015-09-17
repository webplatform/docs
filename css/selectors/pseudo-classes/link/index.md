---
title: ':link'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ':link'
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Used to select and style unvisited links.'
tags:
  - CSS_Selectors
  - CSS
uri: 'css/selectors/pseudo-classes/:link'

---
## Summary

Used to select and style unvisited links.

 User agents commonly display unvisited links differently from previously visited ones. Selectors provides pseudo-classes to distinguish them:

-   The :link pseudo-class applies to links that have not yet been visited.
-   The [:visited](/css/selectors/pseudo-classes/:visited) pseudo-class applies once the link has been visited by the user.

After some amount of time, user agents may choose to return a visited link to the (unvisited) ‘:link’ state.

The two states are mutually exclusive.

## Examples

The following style rule uses the **:link** pseudo-class to set the default [**color**](/css/properties/color) attribute of a link in a document.

``` css
<style>
    A:link { color:#FF0000 }
</style>
```

## Usage

     The :link pseudo-class is often used with :active, :hover and :visited, the pseudo-classes that affect the other states of a link.

The default value of the **:link** pseudo-class is browser-specific. The time period used to define a recent visit also varies by browser.

## Notes

> **Note:** It is possible for style sheet authors to abuse the :link and :visited pseudo-classes to determine which sites a user has visited without the user's consent.

UAs may therefore treat all links as unvisited links, or implement other measures to preserve the user's privacy while rendering visited and unvisited links differently.

## Related specifications

[CSS 2.1](http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes)
:   W3C Recommendation

[Selectors Level 3](http://www.w3.org/TR/css3-selectors/#link)
:   W3C Recommendation

[Selectors Level 4](http://dev.w3.org/csswg/selectors4/#link)
:   W3C Working Draft
