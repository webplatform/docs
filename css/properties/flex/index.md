---
title: flex
tags:
  - CSS
  - Properties
  - Flexbox
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex CSS property specifies the ability of a flex item to alter its dimensions to fill the available space. flex is a shorthand property comprised of the flex-grow, flex-shrink, and flex-basis properties. A flex item can be stretched to use available space proportional to its flex grow factor, or reduced proportional to its flex shrink factor to prevent overflow.'
code_samples:
  - 'http://gist.github.com/5506026'
uri: css/properties/flex

---
# flex

## Summary

The flex CSS property specifies the ability of a flex item to alter its dimensions to fill the available space. flex is a shorthand property comprised of the flex-grow, flex-shrink, and flex-basis properties. A flex item can be stretched to use available space proportional to its flex grow factor, or reduced proportional to its flex shrink factor to prevent overflow.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0 1 auto`
Applies to
:   flex items
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   See individual properties
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `flex`

## Syntax

-   `flex: 3 1 60%`
-   `flex: <flex-grow> <flex-shrink> <flex-basis>`
-   `flex: auto`
-   `flex: initial`
-   `flex: none`

## Values

\<[flex-grow](/css/properties/flex-grow)\> \<[flex-shrink](/css/properties/flex-shrink)\> \<[flex-basis](/css/properties/flex-basis)\>
:   The shorthand value of this property includes the following values:

-   Value of the [flex-grow](/css/properties/flex-grow) property.
-   Value of the [flex-shrink](/css/properties/flex-shrink) property.
-   Value of the [flex-basis](/css/properties/flex-basis) property.

3 1 60%
:   An example of the shorthand values.

-   The flex item grows three times as much as the other flex items to fit a larger container.
-   The flex item shrinks just as much as the other flex items to fit a smaller container.
-   The flex item's initial main size is 60% of its container.

none
:   Equivalent to **0 0 auto**

-   The flex item does not adjust its size to fit the container.
-   The flex item's initial main size is determined by either the [width](/css/properties/width) or [height](/css/properties/height) property, whichever is in the main dimension, as determined by the [flex-direction](/css/properties/flex-flow) property.

auto
:   Equivalent to **1 1 auto**

-   The flex item grows exactly proportional to all of the other flex items to fit a larger container.
-   The flex item shrinks exactly proportional to all of the other flex items to fit a smaller container.
-   The flex item's initial main size is determined by either the [width](/css/properties/width) or [height](/css/properties/height) property, whichever is in the main dimension, as determined by the [flex-direction](/css/properties/flex-flow) property.

initial
:   Equivalent **0 1 auto'**

-   The flex item does not grow with the other flex items to fit a larger container.
-   The flex item shrinks proportional to the other flex items to fit a smaller container.
-   The flex item's initial main size is determined by either the [width](/css/properties/width) or [height](/css/properties/height) property, whichever is in the main dimension, as determined by the [flex-direction](/css/properties/flex-flow) property.

## Examples

The Holy Grail layout CSS: how to set up one layout that covers both desktop and mobile use cases.

``` {.css}
body {
   font: 24px Helvetica;
   background: #999999;
  }

  #main {
   min-height: 800px;
   margin: 0px;
   padding: 0px;
   display: flex;
   flex-flow: row;
   }

  #main > article {
   margin: 4px;
   padding: 5px;
   border: 1px solid #cccc33;
   border-radius: 7pt;
   background: #dddd88;
   flex: 3 1 60%;
   order: 2;
   }

  #main > nav {
   margin: 4px;
   padding: 5px;
   border: 1px solid #8888bb;
   border-radius: 7pt;
   background: #ccccff;
   flex: 1 6 20%;
   order: 1;
   }

  #main > aside {
   margin: 4px;
   padding: 5px;
   border: 1px solid #8888bb;
   border-radius: 7pt;
   background: #ccccff;
   flex: 1 6 20%;
   order: 3;
   }

  header, footer {
   display: block;
   margin: 4px;
   padding: 5px;
   min-height: 100px;
   border: 1px solid #eebb55;
   border-radius: 7pt;
   background: #ffeebb;
   }

  /* Too narrow to support three columns */
  @media all and (max-width: 640px) {

   #main, #page {
    flex-flow: column;
   }

   #main > article, #main > nav, #main > aside {
    /* Return them to document order */
    order: 0;
   }

   #main > nav, #main > aside, header, footer {
    min-height: 50px;
    max-height: 50px;
   }
  }
```

[View live example](http://code.webplatform.org/gist/5506026)

The Holy Grail layout HTML.

``` {.html}
<!DOCTYPE html>
<html lang="en">
  <head>
    <style>
    </style>
  </head>
  <body>
 <header>header</header>

   <article>article</article>
   <nav>nav</nav>
   <aside>aside</aside>
```

    <footer>footer</footer>
     </body>

\</html\>

</pre>
[View live example](http://code.webplatform.org/gist/5506026)

</div>
## Usage

     * Best practice is to always specify a unit for the flex-basis value, i.e. 30em or 60%.

-   The flex shrink factor is multiplied by the flex basis when distributing negative space.

## Notes

-   Negative values are invalid.
-   The initial values of [flex-grow](/css/properties/flex-grow) and [flex-basis](/css/properties/flex-basis) are different from their values when omitted in the **flex** shorthand.
    -   **flex-grow** value when omitted: **1**
    -   **flex-basis** value when omitted: **0**
-   When specifying only the flex-basis, a unitless zero not preceded by two flex factor values, for example, **  0** will be interpreted as a flex factor (probably flex-grow). If you wish to specify only the flex-basis, you must include a unit, for example, a percentage, as in **0%**.

## Related specifications

Specification
:   Status
[CSS Flexible Box Layout Module](http://dev.w3.org/csswg/css-flexbox/#flex)
:   Candidate Recommendation

## See also

### Related articles

#### Flexbox

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   **flex**

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)

### External resources

Also, check out the following live demo sites and article about flexbox:

-   [Flexbox Playground](http://demo.agektmr.com/flexbox/)
-   [Flexy Boxes](http://the-echoplex.net/flexyboxes)
-   [http://tympanus.net/codrops/css\_reference/flexbox/](http://tympanus.net/codrops/css_reference/flexbox/)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](//static.webplatformstaging.org/w/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/Tutorials/Using_CSS_flexible_boxes)

