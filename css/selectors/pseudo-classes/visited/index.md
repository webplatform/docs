---
title: ':visited'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ':visited'
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The\_:visited pseudo-class applies to links the user has visited"
tags:
  - CSS_Selectors
  - CSS
uri: 'css/selectors/pseudo-classes/:visited'

---
## Summary

The :visited pseudo-class applies to links the user has visited

 User agents commonly display unvisited links differently from previously visited ones. Selectors provides pseudo-classes to distinguish them:

-   The `:link` pseudo-class applies to links that have not yet been visited.
-   The `:visited` pseudo-class applies once the link has been visited by the user.

After some amount of time, user agents may choose to return a visited link to the (unvisited) ‘`:link`’ state.

The two states are mutually exclusive.

## Examples

The following style rule uses **:visited** to set the [**color**](/css/properties/color) attribute of visited links in a document.

``` css
a:visited { color:blue }
```

## Usage

     :visited  is often used with :active, :hover, and :link, which are the pseudo-classes that reflect the other states of a link.

The default value of the **:visited** pseudo-class varies by browser, as does the amount of time used to define a recent visit.

## Notes

The pseudo-classes [:link](/css/selectors/pseudo-classes/:link) and :visited can be abused to determine which sites a user has visited.

To preserver their users’ privacy, browsers often implement counter-measures against these abuses, while still rendering visited and unvisited links differently.

## Related specifications

[CSS 2.1](http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes)
:   W3C Recommendation

[Selectors Level 3](http://www.w3.org/TR/css3-selectors/#link)
:   W3C Recommendation

[Selectors Level 4](http://dev.w3.org/csswg/selectors4/#link)
:   W3C Working Draft
