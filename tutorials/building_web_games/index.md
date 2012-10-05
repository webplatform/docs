{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|With the combination of developments in HTML5 and improvements to modern browsers, it's now possible to build high-quality games using web technologies.

In this document, we'll provide you with the tools, frameworks, and tutorials you'll need to create games.  We'll also explain how they should be used and how they fit together.
}}
{{Tutorial
|Content=== 2D Games ==

The <code>canvas</code> element was introduced in HTML5, a low level, procedural model that updates a bitmap and does not have a built-in scene graph. This allows web developers to easily create animation, rich interfaces and games. 

[http://www.caniuse.com/#search=canvas Every major mobile and desktop browser supports the canvas element], allowing you to create rich 2D games on both mobile and desktop. Also, traditional DOM manipulation can be used to create games.

=== Performance Considerations ===

There are important performance considerations to note as you're developing your game, especially on mobile. New HTML5 games sometimes exhibit quirks and low frame rates. Although there are many other benchmark suites that measure JavaScript performance, Facebook has built one focused specifically on key game performance metrics. It's called [http://www.jsgamebench.com/ JSGameBench].

Facebook has also created a series of blog posts that explains performance findings so far, as well as information on how to use the benchmark.

* [https://developers.facebook.com/blog/post/454 The initial Tech Talk]
* [https://www.facebook.com/notes/facebook-engineering/html5-games-01-speedy-sprites/491691753919 HTML5 Games 0.1: Speedy Sprites]
* [https://developers.facebook.com/blog/post/460 HTML5 Games 0.2: Integers are Your Friends]
* [https://developers.facebook.com/blog/post/468 HTML5 Games 0.3: Seeing the Future]
* [https://developers.facebook.com/blog/post/492 HTML5 Games 0.4: Memory]

The main performance issue, especially on mobile, is the lack of hardware acceleration. There are a number of hacks available to force a hardware pipeline. For more information on how to do that, see [http://www.html5rocks.com/en/tutorials/canvas/performance/ Improving HTML5 Canvas Performance]. To understand if you're getting hardware acceleration on iOS, [http://mir.aculo.us/2011/02/08/visualizing-webkits-hardware-acceleration/ you can set a flag in the simulator].

=== Canvas ===
The canvas element was introduced in the HTML5 spec. The following code snippet is an example of how you can use it.

 &lt;canvas id="gameCanvas" width="500" height="500"&gt;
     This text is displayed if your browser does not support HTML5 Canvas.
 &lt;/canvas&gt;

Using JavaScript, you can draw on the canvas.

 var gameCanvas = document.getElementById('gameCanvas'),
     gameCanvasContext = gameCanvas.getContext('2d');
 context.fillStyle = "rgb(255,255,0)";
 context.fillRect(40, 40, 60, 60);

For a comprehensive overview of the canvas tag and what can be done with it, check out this [http://projects.joshy.org/presentations/HTML/CanvasDeepDive/presentation.html "HTML 5 Canvas Deep Dive" tutorial] or the [http://diveintohtml5.org/canvas.html tutorial at Dive Into HTML5]. The canvas element can be interacted with in a variety of ways. A [http://simon.html5.org/dump/html5-canvas-cheat-sheet.html handy cheat sheet] is available to keep track of all of the methods.

There are a number of tutorials available online, including the [http://www.html5rocks.com/en/tutorials/casestudies/onslaught.html case study of Onslaught! Arena] and [http://www.html5rocks.com/en/tutorials/#games others on HTML5 Rocks].

While HTML5 game development is relatively nascent, there are a handful of game engines that are being used actively. We recommend the following engines in order to abstract away the need to write complicated logic for functionality like graphics and physics engines.

=== [http://craftyjs.com/ CraftyJS] ===
CraftyJS is primarily focused on desktop development, including support for legacy browsers like IE6. Working interchangeably with the canvas element and DOM manipulation, it also contains a bunch of extra functionality like collision detection, sprite maps, and animation.

You can learn more about it on the [http://craftyjs.com/ CraftyJS website], or try out some [http://craftyjs.com/demos.php sample games]. It's open source and available on [https://github.com/louisstow/Crafty Github].

=== [http://www.impactjs.com/ Impact] ===
Impact is a game engine that utilizes only the canvas element and runs on both mobile and desktop. It includes functionality to help with collision detection and animation. It also has a level editor and integrates with Box 2D.

You can check it out on the [http://impactjs.com/ Impact website]. Full games are available, including [http://playbiolab.com/ Biolab Disaster] and [http://www.phoboslab.org/ztype/ ZType]. [http://impactjs.com/buy-impact Licenses for Impact] are $99.

=== [http://www.box2d.org/ Box2D] ===
Box2D is a physics engine that was ported from Flash. It's actively supported and works well with other gaming engines like Impact. 

You can learn more about it at the [http://www.box2d.org/ Box2D website]. It's open source and [http://code.google.com/p/box2dweb/ available on Google Code].

=== DOM Manipulation ===
Generally, we recommend using the &lt;canvas&gt; element to create games. The performance is increasingly quick and it gives you more control and flexibility over per-pixel manipulation, making game development easier. However, manipulating the [http://en.wikipedia.org/wiki/Document_Object_Model Document Object Model (DOM)] can have performance benefits depending on what and where you're developing— especially on mobile.

To get a sense of the performance differences, read through [http://blog.frontendforce.com/2010/03/games-development-in-javascript-canvas-vs-dom-benchmark/ this article at Frontend Force] and run some of the tests available.

If you're interested in using DOM manipulation, Crafty JS and [http://www.limejs.com/ Lime JS] are game engines that support this. Lime JS works on desktop and mobile, is open source and [https://github.com/digitalfruit/limejs is available on Github]. Check out the [http://www.limejs.com/static/roundball/index.html Roundball sample game] for an example running Lime JS.

=== Making the Game Load Fast ===
In order to ensure that your game loads quickly, you should package up as many static resources as possible. The fewer network requests your game makes, the faster it will load, especially on mobile. This includes images, Javascript, CSS and anything else that takes another network request to download. 

If you're interested in learning why this is important, read [http://css-tricks.com/158-css-sprites/ this article at CSS Tricks].

There are a couple of tools available that will compile multiple images into a spritesheet for you. First is the [http://spritegen.website-performance.org/ CSS Sprite Generator], a free and open source web-based tool. Also, there's [http://www.texturepacker.com/ Texture Packer], a downloadable tool.

== 3D Game Engine ==

Also built on top of canvas, WebGL is actively being implemented into modern desktop browsers, allowing 3D development. No mobile browsers currently support WebGL. [http://learningwebgl.com/blog/ Learning WebGL] is a great resource to follow the news, discover demos, and know when browsers have started supporting WebGL.

There are a number of 3D WebGL-based engines under active development. We've highlighted some of the top engines below.

=== [https://github.com/mrdoob/three.js#readme Three.js] ===
Three.js is an open source 3D graphics engine that has been used in projects like [http://www.ro.me/ ROME].

You can learn more, try out demos, and download the source at the [https://github.com/mrdoob/three.js Github repo].

Also freely available and open source are [https://github.com/supereggbert/GLGE GLGE] and [https://github.com/cathyatseneca/c3dl C3DL].

=== [http://benvanik.github.com/WebGL-Inspector/ WebGL Inspector] ===
Similar to Firebug, this tool helps you debug WebGL issues. It has functionality like injecting into pages, embedding in an existing application with a single script include, and capturing entire GL frames.

Learn more about it on the [http://benvanik.github.com/WebGL-Inspector/ WebGL Inspector] site.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=Facebook HTML5 Resource Center
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}