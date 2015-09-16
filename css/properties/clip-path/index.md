---
title: clip-path
code_samples:
  - 'http://gist.github.com/6338479'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements. In SVG, applies to container elements (without the \<defs\> element), all graphics elements, and \<clipPath\>'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with \<url\> values made absolute'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'As specified'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The clip-path property prevents a portion of an element from drawing by defining a clipping region.'
tags:
  - CSS
  - Properties
uri: css/properties/clip-path

---
## Summary

The clip-path property prevents a portion of an element from drawing by defining a clipping region.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements. In SVG, applies to container elements (without the \<defs\> element), all graphics elements, and \<clipPath\>

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with \<url\> values made absolute

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   As specified

## Syntax

-   `clip-path: <clip-source>`
-   `clip-path: <basic-shape>`
-   `clip-path: none`

## Values

\<basic-shape\>
:   The shape is computed based on the values of one of *inset, circle, ellipse* or *polygon*. If shape-box is not supplied, then the reference box defaults to margin-box.

-   `inset(<shape-arg>{1,4} [round <border-radius>])`. Defines an inset rectangle. The basic syntax for inset is the same as the margin shorthand syntax (see [margin](/css/properties/margin) for details). The optional border-radius argument defines an inset's rounded corners using the border-radius shorthand syntax (see [border-radius](/css/properties/border-radius) for details).

-   `circle([<shape-radius>] [at <position>])` The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [background-position](/css/properties/background-position) for details).

-   `ellipse([<shape-radius>{2}] [at <position>])` The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [background-position](/css/properties/background-position) for details).

-   `polygon([<fill-rule>,] [<shape-arg> <shape-arg>]# )` The fill-rule is used to determine the interior of the polygon (see the SVG [fill-rule](/svg/attributes/fill-rule) for details). Each pair in the shape-arg represents x and y coordinates of each vertex in the polygon.

\<clip-source\>
:   The `<clip-source>` value may be one of the following.

-   `<url>` A URL reference to a `<clipPath>` element.
-   `child` A keyword to indicate that the last direct child `<clipPath>` element of the element to which the `clip-path` property is applied should be used as the clip source. Equivalent to `select(clipPath:last-of-type)`.
-   `<child-selector>` A functional notation accepting a comma-separated list of compound selectors that represents the first matching `<clipPath>` element in tree order (as defined in [DOM](http://dev.w3.org/fxtf/masking/#DOM)).

none
:   No clipping path is created.

## Examples

The following clip-path definition creates a rectangular clipping path with rounded corners.

``` css
#image {
    clip-path: inset(10% 10% 10% 10% round 20%, 20%);
}
```

The following clip-path definition references a \<clipPath\> element for clipping.

``` css
#image {
    clip-path: url(#clipping);
}
```

A \<clipPath\> element specifies a clipping region. Multiple shapes inside a \<clipPath\> element result in an additive clipping behavior.

Any shape inside the \<clipPath\> element and the \<clipPath\> element itself can be clipped as well. This clipping is exclusive.

``` html
<clipPath id="clipping">
  <circle cx="150" cy="150" r="50" />
  <rect x="150" y="150" width="100" height="100" />
</clipPath>
```

In this example, the Web Platform Docs logo is clipped in two ways; one shows the icon (clipped with a circle) and the other shows the text (clipped with an ellipse).

``` css
img.clipped-icon {
  /**
   * This clips a circle around the image leaving only the icon visible.
   */
  clip-path: circle(30px at 35px 35px);
}

img.clipped-text {
  /**
   * This clips the image leaving only the text visible.
   */
  clip-path: ellipse(65px 30px at 125px 40px);
}
```

[View live example](http://code.webplatform.org/gist/6338479)

The three images that are clipped. The first one (`img.original`) is the original logo. The second one (`img.clipped-icon`) is clipped with a circle and the third one (`img.clipped-text`) is clipped with an ellipse.

``` html


<img class="original" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (original)" title="Web Platform Docs logo (original)" />
<img class="clipped-icon" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (icon only)" title="Web Platform Docs logo (icon only)" />
<img class="clipped-text" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (text only)" title="Web Platform Docs logo (text only)" />
```

</pre>

## Related specifications

[CSS Masking](http://dev.w3.org/fxtf/masking/)
:   Editor's Draft

[SVG 1.1](http://www.w3.org/TR/SVG/)
:   Recommendation
