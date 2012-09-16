{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=== The <canvas> element ==
 
Let's start this tutorial by looking at the <code>&lt;canvas&gt;</code> element itself.
  
<pre>&lt;canvas id="tutorial" width="150" height="150"&gt;&lt;/canvas&gt;

</pre>
  
This looks a lot like the <code>&lt;img&gt;</code> element, the only difference is that it doesn't have the <code>src</code> and <code>alt</code> attributes. The <code>&lt;canvas&gt;</code> element has only two attributes - '''width''' and '''height'''. These are both optional and can also be set using [[DOM]] properties. When no width and height attributes are specified, the canvas will initially be '''300 pixels''' wide and '''150 pixels''' high. The element can be sized arbitrarily by [[CSS]], but during rendering the image is scaled to fit its layout size. (If your renderings seem distorted, try specifying your width and height attributes explicitly in the <code>&lt;canvas&gt;</code> attributes, and not with CSS.)
 
The <code>id</code> attribute isn't specific to the <code>&lt;canvas&gt;</code> element but is one of the default HTML attributes which can be applied to (almost) every HTML element (like <code>class</code> for instance). It's always a good idea to supply an <code>id</code> because this makes it much easier to identify it in our script.
 
The <code>&lt;canvas&gt;</code> element can be styled just like any normal image (margin, border, background, etc). These rules however don't affect the actual drawing on the canvas. We'll see how this is done later in this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.
 
==== Fallback content ====
 
Because the <code>&lt;canvas&gt;</code> element is still relatively new, we need a means of providing fallback content when a browser doesn't support the element.
 
This is very straightforward: we just provide alternative content inside the canvas element. Browsers which don't support <code>&lt;canvas&gt;</code> will ignore the container and render the fallback content inside it. Browsers which do support <code>&lt;canvas&gt;</code> will ignore the content inside the container, and just render the canvas normally.
 
For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content. This can look something like this:
 
<pre>&lt;canvas id="stockGraph" width="150" height="150"&gt;
  current stock price: $3.15 +0.15
&lt;/canvas&gt;

&lt;canvas id="clock" width="150" height="150"&gt;
  &lt;img src="images/clock.png" width="150" height="150" alt=""/&gt;
&lt;/canvas&gt;

</pre>
 
==== Required </canvas> tag ====
 
In the Apple Safari implementation, <code>&lt;canvas&gt;</code> is an element implemented in much the same way <code>&lt;img&gt;</code> is; it does not have an end tag. However, for <code>&lt;canvas&gt;</code> to have widespread use on the web, some facility for fallback content must be provided. Therefore, Mozilla's implementation ''requires'' an end tag (<code>&lt;/canvas&gt;</code>).
 
If fallback content is not needed, a simple <code>&lt;canvas id="foo" ...&gt;&lt;/canvas&gt;</code> will be fully compatible with both Safari and Mozilla -- Safari will simply ignore the end tag.
 
If fallback content is desired, some CSS tricks must be employed to mask the fallback content from Safari (which should render just the canvas), and also to mask the CSS tricks themselves from IE (which should render the fallback content).
 
== The rendering context ==
 
<code>&lt;canvas&gt;</code> creates a fixed size drawing surface that exposes one or more ''rendering contexts'', which are used to create and manipulate the content shown. We'll focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, there is a 3D context ("experimental-webgl") based on OpenGL ES.
 
The <code>&lt;canvas&gt;</code> is initially blank, and to display something a script first needs to access the rendering context and draw on it. The canvas element has a DOM method called <code>getContext</code>, used to obtain the rendering context and its drawing functions. <code>getContext()</code> takes one parameter, the type of context.
 
<pre>var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');

</pre>
 
In the first line we retrieve the canvas DOM node using the [[getElementById]] method. We can then access the drawing context using the <code>getContext</code> method.
 
=== Checking for support ===
 
The fallback content is displayed in browsers which do not support <code>&lt;canvas&gt;</code>; scripts can also check for support when they execute. This can easily be done by testing for the <code>getContext()</code> method. Our code snippet from above becomes something like this:
 
<pre>var canvas = document.getElementById('tutorial');
if (canvas.getContext){
  var ctx = canvas.getContext('2d');
  // drawing code here
} else {
  // canvas-unsupported code here
}

</pre>
 
== A skeleton template ==
 
Here is a minimalistic template, which we'll be using as a starting point for later examples. 
 
<pre>&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Canvas tutorial&lt;/title&gt;
    &lt;script type="text/javascript"&gt;
      function draw(){
        var canvas = document.getElementById('tutorial');
        if (canvas.getContext){
          var ctx = canvas.getContext('2d');
        }
      }
    &lt;/script&gt;
    &lt;style type="text/css"&gt;
      canvas { border: 1px solid black; }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body onload="draw();"&gt;
    &lt;canvas id="tutorial" width="150" height="150"&gt;&lt;/canvas&gt;
  &lt;/body&gt;
&lt;/html&gt;

</pre>
 
If you look at the script you'll see I've made a function called <code>draw</code>, which will get executed once the page finishes loading (via the <code>onload</code> attribute on the <code>body</code> tag). This function could also have been called from a [[setTimeout]], [[setInterval]], or any other event handler function just as long the page has been loaded first.
 
== A simple example ==
 
To start off, here's a simple example that draws two intersecting rectangles, one of which has alpha transparency. We'll explore how this works in more detail in later examples.
 
[[File:canvas ex1.png|right|Two overlapping rectangles on a canvas]]
 
<pre>&lt;html&gt;
 &lt;head&gt;
  &lt;script type="application/javascript"&gt;
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
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body onload="draw();"&gt;
   &lt;canvas id="canvas" width="150" height="150"&gt;&lt;/canvas&gt;
 &lt;/body&gt;
&lt;/html&gt;

</pre>
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en/Canvas_tutorial/Basic_usage
|MSDN_link=
|HTML5Rocks_link=
}}