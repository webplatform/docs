---
title: perspective
code_samples:
  - 'http://gist.github.com/7086839'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'Transformable elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Absolute length or "none".'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "The perspective property defines how far an element is placed from the view on the z-axis, from the screen to the viewer.\n"
tags:
  - CSS
  - Properties
uri: css/properties/perspective

---
## <span>Summary</span>

The perspective property defines how far an element is placed from the view on the z-axis, from the screen to the viewer.

Perspective defines how an object is viewed. In graphic arts, perspective is the representation on a flat surface of what the viewer's eye would see in a 3D space. (See [Wikipedia](http://en.wikipedia.org/wiki/Perspective_(graphical)) for more information about graphical perspective and for related illustrations.)

The illusion of perspective on a flat surface, such as a computer screen, is created by projecting points on the flat surface as they would appear if the flat surface were a window through which the viewer was looking at the object. In discussion of virtual environments, this flat surface is called a projection plane.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   Transformable elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Absolute length or "none".

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `perspective: <length>`
-   `perspective: none`

## <span>Values</span>

none
:   Default.

[\<length\>](/css/data_types/length)
:   The distance the element is placed on the z-axis. Lengths must be positive.

## <span>Examples</span>

The following example shows the difference with transforms, where the first image has a perspective set and the second does not.

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Perspective example</title>
    <style>
      .foo {
        margin: 0 100px;
        float: left;
      }

      .bar {
        perspective: 800px;
      }

      .foo img {
        transform: rotateX(-60deg);
      }
    </style>
  </head>
  <body>
    <div class="foo bar">
      <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" />
    </div>

    <div class="foo baz">
      <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" />
    </div>
  </body>
</html>
```

[View live example](http://code.webplatform.org/gist/7086839)

## <span>Related specifications</span>

[CSS Transforms](http://www.w3.org/TR/css3-transforms/#perspective-property)
:   Working Draft

## <span>See also</span>

### <span>Other articles</span>

-   [Manipulating content with CSS3 transforms - You need some perspective](/tutorials/css_transforms#You_need_some_perspective) by [Mike Sierra](/User:Sierra)

### <span>External resources</span>

-   [CSS 3D Transforms: Interactive Demo](http://sandbox.webpro.nl/css3/3d-transforms-interactive-demo.html) by [Lars Kappert](https://twitter.com/webprolific)
