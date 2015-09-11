---
title: Basic usage
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en/Canvas_tutorial/Basic_usage)'
notes:
  - 'Fix broken links'
readiness: 'Almost Ready'
summary: 'The first part of this tutorial is going to explain how to create a canvas 2D context to draw within. Also discussed are some compatility decisons, which provide more granular browser support.'
tags:
  - Tutorials
  - Canvas
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - getElementById
    - setTimeout
    - setInterval
uri: 'tutorials/canvas/Canvas tutorial/Basic usage'

---
## <span>Summary</span>

The first part of this tutorial is going to explain how to create a canvas 2D context to draw within. Also discussed are some compatility decisons, which provide more granular browser support.

## <span>The \<canvas\> element</span>

Let's start this tutorial by looking at the `<canvas>` element itself.

    <canvas id="tutorial" width="150" height="150"></canvas>

This looks a lot like the `<img>` element, the only difference is that it doesn't have the `src` and `alt` attributes. The `<canvas>` element has only two attributes - **width** and **height**. These are both optional and can also be set using [DOM](/dom) properties. When no width and height attributes are specified, the canvas will initially be **300 pixels** wide and **150 pixels** high. The element can be sized arbitrarily by [CSS](/css), but during rendering the image is scaled to fit its layout size. (If your renderings seem distorted, try specifying your width and height attributes explicitly in the `<canvas>` attributes, and not with CSS.)

The `id` attribute isn't specific to the `<canvas>` element but is one of the default HTML attributes which can be applied to (almost) every HTML element (like `class` for instance). It's always a good idea to supply an `id` because this makes it much easier to identify it in our script.

The `<canvas>` element can be styled just like any normal image (margin, border, background, etc). These rules however don't affect the actual drawing on the canvas. We'll see how this is done later in this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.

#### <span>Fallback content</span>

Because the `<canvas>` element is still relatively new, we need a means of providing fallback content when a browser doesn't support the element.

This is very straightforward: we just provide alternative content inside the canvas element. Browsers which don't support `<canvas>` will ignore the container and render the fallback content inside it. Browsers which do support `<canvas>` will ignore the content inside the container, and just render the canvas normally.

For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content. This can look something like this:

    <canvas id="stockGraph" width="150" height="150">
      current stock price: $3.15 +0.15
    </canvas>

    <canvas id="clock" width="150" height="150">
      <img src="images/clock.png" width="150" height="150" alt=""/>
    </canvas>

#### <span>Required \</canvas\> tag</span>

In the Apple Safari implementation, `<canvas>` is an element implemented in much the same way `<img>` is; it does not have an end tag. However, for `<canvas>` to have widespread use on the web, some facility for fallback content must be provided. Therefore, Mozilla's implementation *requires* an end tag (`</canvas>`).

If fallback content is not needed, a simple `<canvas id="foo" ...></canvas>` will be fully compatible with both Safari and Mozilla -- Safari will simply ignore the end tag.

If fallback content is desired, some CSS tricks must be employed to mask the fallback content from Safari (which should render just the canvas), and also to mask the CSS tricks themselves from IE (which should render the fallback content).

## <span>The rendering context</span>

`<canvas>` creates a fixed size drawing surface that exposes one or more *rendering contexts*, which are used to create and manipulate the content shown. We'll focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, there is a 3D context ("experimental-webgl") based on OpenGL ES.

The `<canvas>` is initially blank, and to display something a script first needs to access the rendering context and draw on it. The canvas element has a DOM method called `getContext`, used to obtain the rendering context and its drawing functions. `getContext()` takes one parameter, the type of context.

    var canvas = document.getElementById('tutorial');
    var ctx = canvas.getContext('2d');

In the first line we retrieve the canvas DOM node using the [getElementById](/w/index.php?title=getElementById&action=edit&redlink=1) method. We can then access the drawing context using the `getContext` method.

### <span>Checking for support</span>

The fallback content is displayed in browsers which do not support `<canvas>`; scripts can also check for support when they execute. This can easily be done by testing for the `getContext()` method. Our code snippet from above becomes something like this:

    var canvas = document.getElementById('tutorial');
    if (canvas.getContext){
      var ctx = canvas.getContext('2d');
      // drawing code here
    } else {
      // canvas-unsupported code here
    }

## <span>A skeleton template</span>

Here is a minimalistic template, which we'll be using as a starting point for later examples.

    <html>
      <head>
        <title>Canvas tutorial</title>
        <script type="text/javascript">
          function draw(){
            var canvas = document.getElementById('tutorial');
            if (canvas.getContext){
              var ctx = canvas.getContext('2d');
            }
          }
        </script>
        <style type="text/css">
          canvas { border: 1px solid black; }
        </style>
      </head>
      <body onload="draw();">
        <canvas id="tutorial" width="150" height="150"></canvas>
      </body>
    </html>

If you look at the script you'll see I've made a function called `draw`, which will get executed once the page finishes loading (via the `onload` attribute on the `body` tag). This function could also have been called from a [setTimeout](/w/index.php?title=setTimeout&action=edit&redlink=1), [setInterval](/w/index.php?title=setInterval&action=edit&redlink=1), or any other event handler function just as long the page has been loaded first.

## <span>A simple example</span>

To start off, here's a simple example that draws two intersecting rectangles, one of which has alpha transparency. We'll explore how this works in more detail in later examples.

![Two overlapping rectangles on a canvas](/assets/public/2/2a/canvas_ex1.png)

    <html>
     <head>
      <script type="application/javascript">
        function draw() {
          var canvas = document.getElementById("canvas");
          if (canvas.getContext) {
            var ctx = canvas.getContext("2d");

            ctx.fillStyle = "rgb(200,0,0)";
            ctx.fillRect (10, 10, 55, 50);

            ctx.fillStyle = "rgba(0, 0, 200, 0.5)";
            ctx.fillRect (30, 30, 55, 50);
          }
        }
      </script>
     </head>
     <body onload="draw();">
       <canvas id="canvas" width="150" height="150"></canvas>
     </body>
    </html>

[\<\<Previous ||](/tutorials/canvas/canvas_tutorial)[Next\>\>](/tutorials/canvas/Canvas_tutorial/Drawing_shapes)