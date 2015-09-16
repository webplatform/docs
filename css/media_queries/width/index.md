---
title: 'width'
compatibility:
  feature: width
  topic: css
notes:
  - 'Add values, syntax, description,, compatibility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The ‘width’ media feature describes the width of the targeted display area of the output device. For continuous media, this is the width of the viewport (as described by CSS2, section 9.1.1 [CSS2.1]) including the size of a rendered scroll bar (if any). For paged media, this is the width of the page box (as described by CSS2, section 13.2 [CSS2.1]).'
tags:
  - CSS
  - Media
  - Feature
uri: 'css/media queries/width'

---
## Summary

The ‘width’ media feature describes the width of the targeted display area of the output device. For continuous media, this is the width of the viewport (as described by CSS2, section 9.1.1 [CSS2.1]) including the size of a rendered scroll bar (if any). For paged media, this is the width of the page box (as described by CSS2, section 13.2 [CSS2.1]).

## Description

The width media query returns the width of the layout viewport, also called the initial containing block. This is equal to the default width of the html element. Thus, it tells you how much space the browser allows your CSS layout to take.

The width media query is one of the two vital ingredients of responsive web design; the other one is the [meta viewport tag](/tutorials/mobile_viewport). The width media query is very reliable across browsers, and using it will not raise compatibility issues.

The width media query is always, in all browsers, equal to document.documentElement.clientWidth.

## Examples

``` css
@media (width:400px){
   /*This code will only be run if the width of the viewport is exactly 400px*/
}
@media (min-width:400px){
   /*This code will only be run if the width of the viewport is at least 400px*/
}
@media (max-width:400px){
   /*This code will only be run if the width of the viewport is at most 400px*/
}
@media screen and (min-width: 400px) and (max-width: 700px){
  /* ... */
}
```

## Related specifications

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

