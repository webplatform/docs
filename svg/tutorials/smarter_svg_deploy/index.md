---
title: SVG deployment
notes:
  - 'Fix a couple of broken links'
readiness: 'Almost Ready'
summary: 'This brief guide shows different ways to deploy SVG, either within HTML or as standalone files, with various options to reference CSS and JavaScript.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/elements/foreignObject
    - svg/attributes/requiredExtensions
uri: 'svg/tutorials/smarter svg deploy'

---
**By Mike Sierra**

## <span>Summary</span>

This brief guide shows different ways to deploy SVG, either within HTML or as standalone files, with various options to reference CSS and JavaScript.

Until recently, SVG was fairly difficult to incorporate with other web content, and there are still many challenges. The HTML5 standard provides a way to insert *inline* regions of SVG into HTML files.

![scr svg html.png](/assets/public/a/aa/scr_svg_html.png)

It translates to this basic HTML markup structure, where CSS and JavaScript may affect both HTML and SVG content:

``` xml
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js">
    </script>
    <svg>
      <!-- define graphics here -->
    </svg>
  </body>
</html>
```

 There are also other ways to do it. You can reference external SVG files, and render them interactively within the HTML using either [**iframe**](/html/elements/iframe), [**embed**](/html/elements/embed), or [**object**](/html/elements/object) tags:

``` xml
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js"></script>
    <iframe src=’graphics.svg’></iframe>
    <embed src=’graphics.svg’></embed>
    <object data=’graphics.svg’ type=’image/svg+xml’></object>
  </body>
</html>
```

 It's also common to reference external SVG files to present static SVG graphics via CSS. The example below shows how you might place a right-aligned navigation arrow within a mobile interface, rendering as crisply as possible on high-resolution handsets:

![scr svg css.png](/assets/public/d/df/scr_svg_css.png)

``` css
 a[href] {
     background-image    : url(img/nav_arrow.svg);
     background-position : center 0 right 10px;
     background-size     : contain;
     display             : block;
     min-height          : 2em;
     border-radius       : 0.5em;
     padding             : 0.5em;
 }
```

 As you will see, you can also use URL anchors to reference individual component graphics that are collected within an SVG file. This assigns a custom bullet shape:

``` css
 ul > li {
    list-style-image     : url(img/components.svg#bullet);
 }
```

 Less common in practice, SVG files can be viewed as standalone files, perhaps as the target of a navigation. Any SVG file or [**svg**](/svg/elements/svg) tag region can reference its own set of CSS and JavaScript, which only applies within the SVG:

![scr svg svg.png](/assets/public/f/f2/scr_svg_svg.png)

This example shows how to embed or reference either CSS or JavaScript from within an SVG file:

``` xml
<?xml version="1.0" standalone="no"?>
  <!-- reference CSS here: -->
<?xml-stylesheet href="css/styles.css" type="text/css"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="700px" height="500px" viewBox="0 0 1000 500">
  <defs>
    <style type="text/css">
        <![CDATA[
            /* embed CSS here */
        ]]>
    </style>
  </defs>
  <script type="application/ecmascript">
      <![CDATA[
          // embed JavaScript here
      ]]>
  </script>
  <!-- or reference JavaScript here: -->
  <script type="application/ecmascript" xlink:href="js/app.js">
  </script>
  <!-- define graphics here -->
</svg>
```

 From within an SVG, you can also reference components from other SVG files. The example that follows shows how you might import a graphic of a cat from another SVG file, then style it *calico* based on referenced CSS:

![scr svg svg2svg.png](/assets/public/e/eb/scr_svg_svg2svg.png)

``` xml
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?xml-stylesheet href="css/svg_styles.css" type="text/css"?>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="1000" height="1000">
    <use xlink:href="components.svg#cat" class="calico"/>
</svg>
```

 You may also be able to use the [**foreignObject**](/w/index.php?title=svg/elements/foreignObject&action=edit&redlink=1) tag to render live HTML content within an SVG graphic environment. This example uses the [**switch**](/svg/elements/switch) tag to test whether the feature works, as recognized by the tag's [**requiredExtensions**](/w/index.php?title=svg/attributes/requiredExtensions&action=edit&redlink=1) attribute. If not, it uses fallback [**text**](/svg/elements/text):

![scr svg svg2html.png](/assets/public/2/23/scr_svg_svg2html.png)

``` xml
<?xml version="1.0" standalone="yes"?>
<svg width="4in" height="3in" version="1.1" xmlns='http://www.w3.org/2000/svg'>
  <desc>use 'switch' to test if foreignObject works, otherwise render fallback 'text' content</desc>
  <switch>
    <foreignObject width="100" height="50" requiredExtensions="http://example.com/SVGExtensions/EmbeddedXHTML">
      <!-- XHTML content goes here -->
      <body xmlns="http://www.w3.org/1999/xhtml">
        <p>Here is a paragraph that requires word wrap</p>
        <iframe src="external.html">...or an iframe...</iframe>
      </body>
    </foreignObject>
    <text font-size="10" font-family="Verdana">
      <tspan x="10" y="10">Here is a paragraph that</tspan>
      <tspan x="10" y="20">requires word wrap.</tspan>
    </text>
  </switch>
</svg>
```

## <span>See also</span>

### <span>Related articles</span>

#### <span>Filters</span>

-   [blur()](/css/functions/blur)

-   [brightness()](/css/functions/brightness)

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   [hue-rotate()](/css/functions/hue-rotate)

-   [invert()](/css/functions/invert)

-   [opacity()](/css/functions/opacity)

-   [saturate()](/css/functions/saturate)

-   [sepia()](/css/functions/sepia)

-   [filter](/css/properties/filter)

-   [feBlend](/svg/elements/feBlend)

-   [feColorMatrix](/svg/elements/feColorMatrix)

-   [feComponentTransfer](/svg/elements/feComponentTransfer)

-   [feComposite](/svg/elements/feComposite)

-   [feConvolveMatrix](/svg/elements/feConvolveMatrix)

-   [feDiffuseLighting](/svg/elements/feDiffuseLighting)

-   [feDisplacementMap](/svg/elements/feDisplacementMap)

-   [feDistantLight](/svg/elements/feDistantLight)

-   [feFlood](/svg/elements/feFlood)

-   [feFuncA](/svg/elements/feFuncA)

-   [feFuncB](/svg/elements/feFuncB)

-   [feFuncG](/svg/elements/feFuncG)

-   [feFuncR](/svg/elements/feFuncR)

-   [feGaussianBlur](/svg/elements/feGaussianBlur)

-   [feImage](/svg/elements/feImage)

-   [feMerge](/svg/elements/feMerge)

-   [feMergeNode](/svg/elements/feMergeNode)

-   [feMorphology](/svg/elements/feMorphology)

-   [feOffset](/svg/elements/feOffset)

-   [fePointLight](/svg/elements/fePointLight)

-   [feSpecularLighting](/svg/elements/feSpecularLighting)

-   [feSpotlight](/svg/elements/feSpotlight)

-   [feTile](/svg/elements/feTile)

-   [feTurbulence](/svg/elements/feTurbulence)

-   **SVG deployment**

-   [SVG filters](/svg/tutorials/smarter_svg_filters)

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)
