{{Page_Title|Styling SVG with CSS}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article covers the basics of styling SVG content with CSS.}}
{{Tutorial
|Content==== Information: SVG ===
 
''SVG'' (Scalable Vector Graphics) is an XML-based language for creating graphics. It can be used for static images, and also for animations and user interfaces.

Like other XML-based languages, SVG supports CSS stylesheets so that you can separate the style of a graphic from its content.
 
Also, stylesheets that you use with other document markup languages can specify the URL of an SVG graphic where an image is required. For example, a stylesheet that you use with an HTML document can specify the URL of an SVG graphic in the value of a <code>background</code> property.

More details

At the time of writing (mid 2011), most modern browsers have basic support for SVG, including Internet Explorer 9 or later. Some SVG features are supported only partially or not at all on some browsers. See the [[SVG tables on caniuse.com]] for an overview of SVG support, or the compatibility tables in the [[SVG element reference]] for support of specific items.

 You can add SVG support to other versions by installing a plugin such as the one provided by [[Adobe]].

=== Action: An SVG demonstration ===

<ol>
<li> 
<p>Make a new SVG document as a plain text file, <code>doc8.svg</code>. Copy and paste the content from here, making sure that you scroll to get all of it:</p>
  
<pre>&lt;?xml version="1.0" standalone="no"?&gt;

&lt;?xml-stylesheet type="text/css" href="style8.css"?&gt;

&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;

&lt;svg width="600px" height="600px" viewBox="-300 -300 600 600"
  xmlns="http://www.w3.org/2000/svg" version="1.1"
  xmlns:xlink="http://www.w3.org/1999/xlink"&gt;

&lt;title&gt;SVG demonstration&lt;/title&gt;
&lt;desc&gt;Mozilla CSS Getting Started - SVG demonstration&lt;/desc&gt;

&lt;defs&gt;
  &lt;g id="segment" class="segment"&gt;
    &lt;path class="segment-fill" d="M0,0 v-200 a40,40 0 0,0 -62,10 z"/&gt;
    &lt;path class="segment-edge" d="M0,-200 a40,40 0 0,0 -62,10"/&gt;
    &lt;/g&gt;
  &lt;g id="quadrant"&gt;
    &lt;use xlink:href="#segment"/&gt;
    &lt;use xlink:href="#segment" transform="rotate(18)"/&gt;
    &lt;use xlink:href="#segment" transform="rotate(36)"/&gt;
    &lt;use xlink:href="#segment" transform="rotate(54)"/&gt;
    &lt;use xlink:href="#segment" transform="rotate(72)"/&gt;
    &lt;/g&gt;
  &lt;g id="petals"&gt;
    &lt;use xlink:href="#quadrant"/&gt;
    &lt;use xlink:href="#quadrant" transform="rotate(90)"/&gt;
    &lt;use xlink:href="#quadrant" transform="rotate(180)"/&gt;
    &lt;use xlink:href="#quadrant" transform="rotate(270)"/&gt;
    &lt;/g&gt;
  &lt;radialGradient id="fade" cx="0" cy="0" r="200"
      gradientUnits="userSpaceOnUse"&gt;
    &lt;stop id="fade-stop-1" offset="33%"/&gt;
    &lt;stop id="fade-stop-2" offset="95%"/&gt;
    &lt;/radialGradient&gt;
  &lt;/defs&gt;

&lt;text id="heading" x="-280" y="-270"&gt;
  SVG demonstration&lt;/text&gt;
&lt;text  id="caption" x="-280" y="-250"&gt;
  Move your mouse pointer over the flower.&lt;/text&gt;

&lt;g id="flower"&gt;
  &lt;circle id="overlay" cx="0" cy="0" r="200"
    stroke="none" fill="url(#fade)"/&gt;
  &lt;use id="outer-petals" xlink:href="#petals"/&gt;
  &lt;use id="inner-petals" xlink:href="#petals"
    transform="rotate(9) scale(0.33)"/&gt;
  &lt;/g&gt;

&lt;/svg&gt;</pre>
</li>
<li>
<p>Make a new CSS file, <code>style8.css</code>. Copy and paste the content from here, making sure that you scroll to get all of it:
  
<pre>/*** SVG demonstration ***/

/* page */
svg {
  background-color: beige;
  }

#heading {
  font-size: 24px;
  font-weight: bold;
  }

#caption {
  font-size: 12px;
  }

/* flower */
#flower:hover {
  cursor: crosshair;
  }

/* gradient */
#fade-stop-1 {
  stop-color: blue;
  }

#fade-stop-2 {
  stop-color: white;
  }

/* outer petals */
#outer-petals {
  opacity: .75;
  }

#outer-petals .segment-fill {
  fill: azure;
  stroke: lightsteelblue;
  stroke-width: 1;
  }

#outer-petals .segment-edge {
  fill: none;
  stroke: deepskyblue;
  stroke-width: 3;
  }

#outer-petals .segment:hover &gt; .segment-fill {
  fill: plum;
  stroke: none;
  }

#outer-petals .segment:hover &gt; .segment-edge {
  stroke: slateblue;
  }

/* inner petals */
#inner-petals .segment-fill {
  fill: yellow;
  stroke: yellowgreen;
  stroke-width: 1;
  }

#inner-petals .segment-edge {
  fill: none;
  stroke: yellowgreen;
  stroke-width: 9;
  }

#inner-petals .segment:hover &gt; .segment-fill {
  fill: darkseagreen;
  stroke: none;
  }

#inner-petals .segment:hover &gt; .segment-edge {
  stroke: green;
}</pre>
  
<p>Open the document in your SVG-enabled browser. Move your mouse pointer over the graphic.</p>
</li>
</ol>

<p class="note">Note: add dabblet or screenshots to demonstrate this?</p> 

Notes:
 
* The SVG document links the styesheet in the usual way.
* SVG has its own CSS properties and values. Some of them are similar to CSS properties for HTML.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections===Exercise question==

Change the stylesheet so that the inner petals all turn pink when the mouse pointer is over any one of them, without changing the way the outer petals work.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/SVG_and_CSS
|MSDN_link=
|HTML5Rocks_link=
}}