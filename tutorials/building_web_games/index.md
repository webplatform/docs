---
title: Building web games
attributions:
  - 'Facebook HTML5 Resource Center.'
readiness: 'Ready to Use'
summary: "With the combination of developments in HTML5 and improvements to modern browsers, it's now possible to build high-quality games using web technologies.\n"
tags:
  - Tutorials
  - Canvas
  - JavaScript
  - Mobile
  - Performance
uri: 'tutorials/building web games'

---
## <span>Summary</span>

With the combination of developments in HTML5 and improvements to modern browsers, it's now possible to build high-quality games using web technologies.

In this document, we'll provide you with the tools, frameworks, and tutorials you'll need to create games. We'll also explain how they should be used and how they fit together.

## <span>2D Games</span>

The `canvas` element was introduced in HTML5, a low level, procedural model that updates a bitmap and does not have a built-in scene graph. This allows web developers to easily create animation, rich interfaces and games.

[Every major mobile and desktop browser supports the canvas element](http://www.caniuse.com/#search=canvas), allowing you to create rich 2D games on both mobile and desktop. Also, traditional DOM manipulation can be used to create games.

### <span>Performance Considerations</span>

There are important performance considerations to note as you're developing your game, especially on mobile. New HTML5 games sometimes exhibit quirks and low frame rates. Although there are many other benchmark suites that measure JavaScript performance, Facebook has built one focused specifically on key game performance metrics. It's called [JSGameBench](http://www.jsgamebench.com/).

Facebook has also created a series of blog posts that explains performance findings so far, as well as information on how to use the benchmark.

-   [The initial Tech Talk](https://developers.facebook.com/blog/post/454)
-   [HTML5 Games 0.1: Speedy Sprites](https://www.facebook.com/notes/facebook-engineering/html5-games-01-speedy-sprites/491691753919)
-   [HTML5 Games 0.2: Integers are Your Friends](https://developers.facebook.com/blog/post/460)
-   [HTML5 Games 0.3: Seeing the Future](https://developers.facebook.com/blog/post/468)
-   [HTML5 Games 0.4: Memory](https://developers.facebook.com/blog/post/492)

The main performance issue, especially on mobile, is the lack of hardware acceleration. There are a number of hacks available to force a hardware pipeline. For more information on how to do that, see [Improving HTML5 Canvas Performance](http://www.html5rocks.com/en/tutorials/canvas/performance/). To understand if you're getting hardware acceleration on iOS, [you can set a flag in the simulator](http://mir.aculo.us/2011/02/08/visualizing-webkits-hardware-acceleration/).

### <span>Canvas</span>

The canvas element was introduced in the HTML5 spec. The following code snippet is an example of how you can use it.

    <canvas id="gameCanvas" width="500" height="500">
        This text is displayed if your browser does not support HTML5 Canvas.
    </canvas>

Using JavaScript, you can draw on the canvas.

    var gameCanvas = document.getElementById('gameCanvas'),
        gameCanvasContext = gameCanvas.getContext('2d');
    context.fillStyle = "rgb(255,255,0)";
    context.fillRect(40, 40, 60, 60);

For a comprehensive overview of the canvas tag and what can be done with it, check out this ["HTML 5 Canvas Deep Dive" tutorial](http://projects.joshy.org/presentations/HTML/CanvasDeepDive/presentation.html) or the [tutorial at Dive Into HTML5](http://diveintohtml5.org/canvas.html). The canvas element can be interacted with in a variety of ways. A [handy cheat sheet](http://simon.html5.org/dump/html5-canvas-cheat-sheet.html) is available to keep track of all of the methods.

There are a number of tutorials available online, including the [case study of Onslaught! Arena](http://www.html5rocks.com/en/tutorials/casestudies/onslaught.html) and [others on HTML5 Rocks](http://www.html5rocks.com/en/tutorials/#games).

While HTML5 game development is relatively nascent, there are a handful of game engines that are being used actively. We recommend the following engines in order to abstract away the need to write complicated logic for functionality like graphics and physics engines.

### <span>[CraftyJS](http://craftyjs.com/)</span>

CraftyJS is primarily focused on desktop development, including support for legacy browsers like IE6. Working interchangeably with the canvas element and DOM manipulation, it also contains a bunch of extra functionality like collision detection, sprite maps, and animation.

You can learn more about it on the [CraftyJS website](http://craftyjs.com/), or try out some [sample games](http://craftyjs.com/demos.php). It's open source and available on [GitHub](https://github.com/louisstow/Crafty).

### <span>[Impact](http://www.impactjs.com/)</span>

Impact is a game engine that utilizes only the canvas element and runs on both mobile and desktop. It includes functionality to help with collision detection and animation. It also has a level editor and integrates with Box 2D.

You can check it out on the [Impact website](http://impactjs.com/). Full games are available, including [Biolab Disaster](http://playbiolab.com/) and [ZType](http://www.phoboslab.org/ztype/). [Licenses for Impact](http://impactjs.com/buy-impact) are \$99.

### <span>[Box2D](http://www.box2d.org/)</span>

Box2D is a physics engine that was ported from Flash. It's actively supported and works well with other gaming engines like Impact.

You can learn more about it at the [Box2D website](http://www.box2d.org/). It's open source and [available on Google Code](http://code.google.com/p/box2dweb/).

### <span>DOM Manipulation</span>

Generally, we recommend using the \<canvas\> element to create games. The performance is increasingly quick and it gives you more control and flexibility over per-pixel manipulation, making game development easier. However, manipulating the [Document Object Model (DOM)](http://en.wikipedia.org/wiki/Document_Object_Model) can have performance benefits depending on what and where you're developing— especially on mobile.

To get a sense of the performance differences, read through [this article at Frontend Force](http://blog.frontendforce.com/2010/03/games-development-in-javascript-canvas-vs-dom-benchmark/) and run some of the tests available.

If you're interested in using DOM manipulation, Crafty JS and [Lime JS](http://www.limejs.com/) are game engines that support this. Lime JS works on desktop and mobile, is open source and [is available on GitHub](https://github.com/digitalfruit/limejs). Check out the [Roundball sample game](http://www.limejs.com/static/roundball/index.html) for an example running Lime JS.

### <span>Making the Game Load Fast</span>

In order to ensure that your game loads quickly, you should package up as many static resources as possible. The fewer network requests your game makes, the faster it will load, especially on mobile. This includes images, Javascript, CSS and anything else that takes another network request to download.

If you're interested in learning why this is important, read [this article at CSS Tricks](http://css-tricks.com/158-css-sprites/).

There are a couple of tools available that will compile multiple images into a spritesheet for you. First is the [CSS Sprite Generator](http://spritegen.website-performance.org/), a free and open source web-based tool. Also, there's [Texture Packer](http://www.texturepacker.com/), a downloadable tool.

## <span>3D Game Engines</span>

Also built on top of canvas, WebGL is actively being implemented into modern desktop browsers, allowing 3D development. No mobile browsers currently support WebGL. [Learning WebGL](http://learningwebgl.com/blog/) is a great resource to follow the news, discover demos, and know when browsers have started supporting WebGL.

There are a number of 3D WebGL-based engines under active development. We've highlighted some of the top engines below.

### <span>[Three.js](https://github.com/mrdoob/three.js#readme)</span>

Three.js is an open source 3D graphics engine that has been used in projects like [ROME](http://www.ro.me/).

You can learn more, try out demos, and download the source at the [GitHub repo](https://github.com/mrdoob/three.js).

Also freely available and open source are [GLGE](https://github.com/supereggbert/GLGE) and [C3DL](https://github.com/cathyatseneca/c3dl).

### <span>[WebGL Inspector](http://benvanik.github.com/WebGL-Inspector/)</span>

Similar to Firebug, this tool helps you debug WebGL issues. It has functionality like injecting into pages, embedding in an existing application with a single script include, and capturing entire GL frames.

Learn more about it on the [WebGL Inspector](http://benvanik.github.com/WebGL-Inspector/) site.