{{Page_Title|Converting Wordico from Flash to HTML5}}
{{Flags}}
{{Byline
|Name=Adam Mark & Adrian Gould
}}
{{Summary_Section}}
{{Tutorial
|Content=<h2 id="toc-introduction">Introduction</h2>

When we converted our [http://www.wordico.com Wordico] crossword game from Flash to HTML5, our first task was to unlearn everything we knew about creating a rich user experience in the browser. While Flash offered a single, comprehensive API for all aspects of application development—from vector drawing to polygon hit detection to XML parsing—HTML5 offered a jumble of specifications with varying browser support. We also wondered if HTML, a document-specific language, and CSS, a box-centric language, were suitable for building a game. Would the game display uniformly across browsers, as it did in Flash, and would it look and behave as nicely? For Wordico, the answer was ''yes.''

<h2 id="toc-vectorvictor">What's your vector, Victor?</h2>

We developed the original version of Wordico using only vector graphics: lines, curves, fills, and gradients. The result was both highly compact and infinitely scalable:

 [[Image:wordico-flash-wireframe.jpg|600px|Wordico Wireframe]] In Flash, every display object was made of vector shapes.

We also took advantage of the Flash timeline to create objects having multiple states. For example, we used nine named keyframes for the <code>Space</code> object:

 [[Image:wordico-flash-space.png]] A triple-letter space in Flash.

In HTML5, however, we use a bitmapped sprite:

 [[Image:wordico-html-space.png]] A PNG sprite showing all nine spaces.

To create the 15x15 gameboard from individual spaces, we iterate over a 225-character string notation in which each space is represented by a different character (such as "t" for triple letter and "T" for triple word). This was a straightforward operation in Flash; we simply stamped out spaces and arranged them in a grid:

 
 var spaces:Array = new Array();
 
 for (var i:int = 0; i < 225; i++) {
   var space:Space = new Space(i, layout.charAt(i));
   ...
   spaces.push(addChild(space));
 }
 
 LayoutUtil.grid(spaces, 15);

In HTML5, it's a bit more complicated. We use the [http://diveintohtml5.info/canvas.html <code><canvas></code> element], a bitmap drawing surface, to paint the gameboard one square at a time. The first step is to load the image sprite. Once it's loaded, we iterate through the layout notation, drawing a different portion of the image with each iteration:

 
 var x = 0;  // x coordinate
 var y = 0;  // y coordinate
 var w = 35; // width and height of a space
 
 for (var i = 0; i < 225; i++) {
   if (i && i % 15 == 0) {
     x = 0;
     y += w;
   }
 
   var imageX = "_dDFtTqQxm".indexOf(layout.charAt(i)) * 70;
 
   canvas.drawImage("spaces.png", imageX, 0, 70, 70, x, y, w, w);
 
   x += w;
 }

Here's the result in the web browser. Note that the canvas itself has a CSS drop shadow:

 [[Image:wordico-board.png]] In HTML5, the gameboard is a single canvas element.

Converting the tile object was a similar exercise. In Flash, we used [http://livedocs.adobe.com/flash/9.0/ActionScriptLangRefV3/flash/text/TextField.html text fields] and vector shapes:

 [[Image:wordico-flash-tile.png]] The Flash tile was a combination of text fields and vector shapes.

In HTML5, we combine three image sprites on a single <code><canvas></code> element at runtime:

 [[Image:wordico-html-tile.png]] The HTML tile is a composite of three images.

Now we have 100 canvases (one for each tile) plus a canvas for the gameboard. Here's the markup for an "H" tile:

 
 <canvas width="35" height="35" class="tile tile-racked" title="H-2"/>

Here's the corresponding CSS:

 
 .tile {
   width: 35px;
   height: 35px;
   position: absolute;
   cursor: pointer;
   z-index: 1000;
 }
 
 .tile-drag {
   -moz-box-shadow: 1px 1px 7px rgba(0,0,0,0.8);
   -webkit-box-shadow: 1px 1px 7px rgba(0,0,0,0.8);
   -moz-transform: scale(1.10);
   -webkit-transform: scale(1.10);
   -webkit-box-reflect: 0px;
   opacity: 0.85;
 }
 
 .tile-locked {
   cursor: default;
 }
 
 .tile-racked {
   -webkit-box-reflect: below 0px -webkit-gradient(linear, 0% 0%, 0% 100%,
     from(transparent), color-stop(0.70, transparent), to(white));
 }

We apply CSS3 effects when the tile is being dragged (shadow, opacity, and scaling) and when the tile is sitting on the rack (reflection):

 [[Image:wordico-html-tiles.png]] The dragged tile is slightly larger, slightly transparent, and has a drop shadow.

Using raster images has some obvious advantages. First, the result is pixel-precise. Second, these images can be cached by the browser. Third, with a little extra work, we can swap out the images to create new tile designs—such as a metal tile—and this design work can be done in Photoshop instead of in Flash.

The downside? By using images, we give up programmatic access to the text fields. In Flash, it was a simple operation to change the color or other properties of the type; in HTML5, these properties are baked into the images themselves. (We tried HTML text, but it required a lot of extra markup and CSS. We also tried canvas text, but the results were inconsistent across browsers.)

<h2 id="toc-fuzzylogic">Fuzzy logic</h2>

We wanted to make full use of the browser window at any size—and avoid scrolling. This was a relatively simple operation in Flash, since the entire game was drawn in vectors and could be scaled up or down without losing fidelity. But it was trickier in HTML. We tried using CSS scaling but ended up with a blurred canvas:

 [[Image:wordico-html-canvas.png]] CSS scaling (left) vs. redrawing (right).

Our solution is to redraw the gameboard, rack, and tiles whenever the user resizes the browser:

 
 window.onresize = function (evt) {
   ...
   gameboard.setConstraints(boardWidth, boardWidth);
 
   ...
   rack.setConstraints(rackWidth, rackHeight);
 
   ...
   tileManager.resizeTiles(tileSize);
 });

We end up with crisp images and pleasing layouts at any screen size:

 [[Image:wordico-html-scale.jpg]] The gameboard fills the vertical space; other page elements flow around it.

<h2 id="toc-gettothepoint">Get to the point</h2>

Since each tile is absolutely positioned and must align precisely with the gameboard and rack, we need a reliable positioning system. We use two functions, <code>Bounds</code> and <code>Point</code>, to help manage the location of elements in the global space (the HTML page). <code>Bounds</code> describes a rectangular area on the page, while <code>Point</code> describes an ''x,y'' coordinate relative to the top left corner of the page (0,0), otherwise known as the registration point.

With <code>Bounds</code>, we can detect the intersection of two rectangular elements (such as when a tile crosses the rack) or whether a rectangular area (such as a double-letter space) contains an arbitrary point (such as the center point of a tile). Here's the implementation of Bounds:

 
 // bounds.js
 function Bounds(element) {
   var x = element.offsetLeft;
   var y = element.offsetTop;
   var w = element.offsetWidth;
   var h = element.offsetHeight;
 
   this.left = x;
   this.right = x + w;
   this.top = y;
   this.bottom = y + h;
   this.width = w;
   this.height = h;
   this.x = x;
   this.y = y;
   this.midx = x + (w / 2);
   this.midy = y + (h / 2);
   this.topleft = new Point(x, y);
   this.topright = new Point(x + w, y);
   this.bottomleft = new Point(x, y + h);
   this.bottomright = new Point(x + w, y + h);
   this.middle = new Point(x + (w / 2), y + (h / 2));
 }
 
 Bounds.prototype.contains = function (point) {
   return point.x > this.left &&
     point.x < this.right &&
     point.y > this.top &&
     point.y < this.bottom;
 }
 
 Bounds.prototype.intersects = function (bounds) {
   return this.contains(bounds.topleft) {{!}}{{!}}
     this.contains(bounds.topright) {{!}}{{!}}
     this.contains(bounds.bottomleft) {{!}}{{!}}
     this.contains(bounds.bottomright) {{!}}{{!}}
     bounds.contains(this.topleft) {{!}}{{!}}
     bounds.contains(this.topright) {{!}}{{!}}
     bounds.contains(this.bottomleft) {{!}}{{!}}
     bounds.contains(this.bottomright);
 }
 
 Bounds.prototype.toString = function () {
   return [this.x, this.y, this.width, this.height].join(",");
 }

We use <code>Point</code> to determine the absolute coordinate (top-left corner) of any element on the page or of a mouse event. <code>Point</code> also contains methods for calculating distance and direction, which are necessary for creating animation effects. Here's the implementation of <code>Point</code><nowiki>:</nowiki>

 
 // point.js
 
 function Point(x, y) {
   this.x = x;
   this.y = y;
 }
 
 Point.prototype.distance = function (point) {
   var a = point.x - this.x;
   var b = point.y - this.y;
 
   return Math.sqrt(Math.pow(a, 2) + Math.pow(b, 2));
 }
 
 Point.prototype.distanceX = function (point) {
   return Math.abs(this.x - point.x);
 }
 
 Point.prototype.distanceY = function (point) {
   return Math.abs(this.y - point.y);
 }
 
 Point.prototype.interpolate = function (point, pct) {
   var x = this.x + ((point.x - this.x) * pct);
   var y = this.y + ((point.y - this.y) * pct);
 
   return new Point(x, y);
 }
 
 Point.prototype.offset = function (x, y) {
   return new Point(this.x + x, this.y + y);
 }
 
 Point.prototype.vector = function (point) {
   return new Point(point.x - this.x, point.y - this.y);
 }
 
 Point.prototype.toString = function () {
   return this.x + "," + this.y;
 }
 
 // static
 Point.fromElement = function (element) {
   return new Point(element.offsetLeft, element.offsetTop);
 }
 
 // static
 Point.fromEvent = function (evt) {
   return new Point(evt.x {{!}}{{!}} evt.clientX, evt.y {{!}}{{!}} evt.clientY);
 }

These functions form the basis of drag-and-drop and animation capabilities. For example, we use <code>Bounds.intersects()</code> to determine if a tile overlaps a space on the gameboard; we use <code>Point.vector()</code> to determine the direction of a dragged tile; and we use <code>Point.interpolate()</code> in combination with a timer to create a motion tween, or easing effect.

<h2 id="toc-gowiththeflow">Go with the flow</h2>

While fixed-size layouts are easier to produce in Flash, fluid layouts are much easier to generate with HTML and the CSS box model. Consider the following grid view, with its variable width and height:

 [[Image:wordico-html-grid.jpg]] This layout has no fixed dimensions: thumbnails flow left to right, top to bottom.

Or consider the chat panel. The Flash version required multiple event handlers to respond to mouse actions, a mask for the scrollable area, math for computing the scroll position, and a lot of other code to glue it together.

 [[Image:xwordico-flash-chat.jpg.pagespeed.ic._PIgSdvpA0.jpg]] The chat panel in Flash was pretty but complex.

The HTML version, by comparison, is just a <code>&lt;div></code> with a fixed height and the overflow property set to hidden. Scrolling costs us nothing.

 [[Image:wordico-html-chat.jpg]] The CSS box model at work.

In cases like this—ordinary layout tasks—HTML and CSS outshine Flash.

<h2 id="toc-canyouhearmenow">Can you hear me now?</h2>

We struggled with the <code><audio></code> tag—it simply wasn't capable of playing short sounds effects repeatedly in certain browsers. We tried two workarounds. First, we padded the sound files with dead air to make them longer. Then we tried alternating playback across multiple audio channels. Neither technique was completely effective or elegant.

Ultimately we decided to roll our own Flash audio player and use HTML5 audio as a fallback. Here's the basic code in Flash:

 
 var sounds = new Array();
 
 function playSound(path:String):void {
   var sound:Sound = sounds[path];
 
   if (sound == null) {
     sound = new Sound();
     sound.addEventListener(Event.COMPLETE, function (evt:Event) {
       sound.play();
     });
     sound.load(new URLRequest(path));
     sounds[path] = sound;
   }
   else {
     sound.play();
   }
 }
 
 ExternalInterface.addCallback("playSound", playSound);

In JavaScript, we attempt to detect the embedded Flash player. If that fails, we create an <code><audio></code> node for each sound file:

 
 function play(String soundId) {
   var src = "/audio/" + soundId + ".mp3";
 
   // Flash
   try {
     var swf = window["swfplayer"] {{!}}{{!}} document["swfplayer"];
     swf.playSound(src);
   }
   // or HTML5 audio
   catch (e) {
     var sound = document.getElementById(soundId);
     if (sound == null {{!}}{{!}} sound == undefined) {
       var sound = document.createElement("audio");
       sound.id = soundId;
       sound.src = src;
       document.body.appendChild(sound);
     }
     sound.play();
   }
 }

Note that this works for MP3 files only—we never bothered to support OGG. We hope the industry will settle on a single format in the near future.

<h2 id="toc-pollposition">Poll position</h2>

We use the same technique in HTML5 as we did in Flash to refresh the game state: every 10 seconds, the client asks the server for updates. If the game state has changed since the last poll, the client receives and handles the changes; otherwise, nothing happens. This traditional polling technique is acceptable, if not quite elegant. However, we'd like to switch to [http://en.wikipedia.org/wiki/Long_polling#Long_polling long polling] or [http://en.wikipedia.org/wiki/Web_Sockets WebSockets] as the game matures and users come to expect real-time interaction over the network. WebSockets, in particular, would present many opportunities to enhance the game play.

<h2 id="toc-whatatool">What a tool!</h2>

We used [http://code.google.com/webtoolkit/ Google Web Toolkit] (GWT) to develop both the front-end user interface and back-end control logic (authentication, validation, persistence, and so on). The JavaScript itself is compiled from Java source code. For example, the Point function is adapted from <code>Point.java</code><nowiki>:</nowiki>

 
 package com.wordico.client.view.layout;
 
 import com.google.gwt.dom.client.Element;
 import com.google.gwt.dom.client.NativeEvent;
 import com.google.gwt.event.dom.client.DomEvent;
 
 public class Point {
   public double x;
   public double y;
 
   public Point(double x, double y) {
     this.x = x;
     this.y = y;
   }
 
   public double distance(Point point) {
     double a = point.x - this.x;
     double b = point.y - this.y;
 
     return Math.sqrt(Math.pow(a, 2) + Math.pow(b, 2));
   }
   ...
 }

Some UI classes have corresponding template files in which page elements are "bound" to class members. For example, <code>ChatPanel.ui.xml</code> corresponds to <code>ChatPanel.java</code><nowiki>:</nowiki>

 
 <!DOCTYPE ui:UiBinder SYSTEM "http://dl.google.com/gwt/DTD/xhtml.ent">
 
 <ui:UiBinder
   xmlns:ui="urn:ui:com.google.gwt.uibinder"
   xmlns:g="urn:import:com.google.gwt.user.client.ui"
   xmlns:w="urn:import:com.wordico.client.view.widget">
 
   <g:HTMLPanel>
    <div class="palette">
     <g:ScrollPanel ui:field="messagesScroll">
        <g:FlowPanel ui:field="messagesFlow"></g:FlowPanel>
     </g:ScrollPanel>
     <g:TextBox ui:field="chatInput"></g:TextBox>
    </div>
   </g:HTMLPanel>
 
 </ui:UiBinder>

The full details are beyond the scope of this article, but we encourage you to check out GWT for your next HTML5 project.

Why use Java? First, for strict typing. While dynamic typing is useful in JavaScript—for example, the ability of an array to hold values of different types—it can be a headache in large, complex projects. Second, for refactoring capabilities. Consider how you'd change a JavaScript method signature across thousands of lines of code—not easily! But with a good Java IDE, it's a snap. Finally, for testing purposes. Writing unit tests for Java classes beats the time-honored technique of "save and refresh."

<h2 id="toc-summary">Summary</h2>

Except for our audio troubles, HTML5 greatly exceeded our expectations. Not only does Wordico look as good as it did in Flash, it's every bit as fluid and responsive. We couldn't have done it without Canvas and CSS3. Our next challenge: adapting Wordico for mobile use.

Except as otherwise [http://code.google.com/policies.html#restrictions noted], the content of this page is licensed under the [http://creativecommons.org/licenses/by/3.0/ Creative Commons Attribution 3.0 License], and code samples are licensed under the [http://www.apache.org/licenses/LICENSE-2.0 Apache 2.0 License].
}}
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}