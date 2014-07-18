{{Page_Title|SVG fonts}}
{{Flags
|State=In Progress
|Editorial notes=Needs content review, fix multiple broken links
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article covers the creation and usage of SVG fonts.}}
{{Tutorial
|Content=When SVG was specified support for web fonts was far from being expected. Since the correct font is however crucial for the rendering of a graphic, it was decided to add a font description technology to SVG. It was not meant to concur with other formats like PostScript or OTF, but as a simple means of embedding glyph information for rendering engines.
 
SVG Fonts browser support covers all modern browsers (desktop and mobile) except Firefox and Internet Explorer. Firefox has [[postponed implementation indefinitely]] to concentrate on [[WOFF]]. However, other tools, like the [[Adobe SVG Viewer]] plugin, Batik and in parts Inkscape support them. 

The base for defining an SVG font is the {{ SVGElement("font") }} element.
 
== Defining a font ==
 
There are some elements involved in getting all information together, that is needed for a font. I will first show an example declaration (the one [[from the specification]]) and afterwards explain the details.
 
<pre>&lt;font id="Font1" horiz-adv-x="1000"&gt;
  &lt;font-face font-family="Super Sans" font-weight="bold" font-style="normal"
      units-per-em="1000" cap-height="600" x-height="400"
      ascent="700" descent="300"
      alphabetic="0" mathematical="350" ideographic="400" hanging="500"&gt;
    &lt;font-face-src&gt;
      &lt;font-face-name name="Super Sans Bold"/&gt;
    &lt;/font-face-src&gt;
  &lt;/font-face&gt;
  &lt;missing-glyph&gt;&lt;path d="M0,0h200v200h-200z"/&gt;&lt;/missing-glyph&gt;
  &lt;glyph unicode="!" horiz-adv-x="300"&gt;&lt;!-- Outline of exclam. pt. glyph --&gt;&lt;/glyph&gt;
  &lt;glyph unicode="@"&gt;&lt;!-- Outline of @ glyph --&gt;&lt;/glyph&gt;
  &lt;!-- more glyphs --&gt;
&lt;/font&gt;</pre>
 
We start with the {{ SVGElement("font") }} element. It bears an id attribute, that is needed if you want to reference it via URI (see below). The <code>horiz-adv-x</code> attribute determines, how wide a character is on average compared to the path definitions of the single glyphs. The value <code>1000</code> sets a reasonable value to work in. There are several accompanying attributes, that help further defining the basic glyph-box layout.
 
The {{ SVGElement("font-face") }} element is the counterpart of the CSS [[@font-face]] declaration. It defines basic properties of the final font, as how to classify its weight, style and so forth. In the example above the first and most important to be defined is <code>font-family</code>. Its value can then be referenced in CSS and SVG <code>font-family</code> properties. The <code>font-weight</code> and <code>font-style</code> attributes have the same purpose. All following attributes are rendering instructions to the font layout engine, for example, how much of the glyphs' overall height are [[ascenders]].

Its child, the {{ SVGElement("font-face-src") }} element, corresponds to CSS' <code>src</code> property in <code>@font-face</code> declarations. You can point to external sources for font declarations by means of its children {{ SVGElement("font-face-name") }} and {{ SVGElement("font-face-uri") }}. The example states, that if the renderer has a local font at hand named "Super Sans Bold", it should use this instead.
 
Following {{ SVGElement("font-face-src") }} is a {{ SVGElement("missing-glyph") }} element. This declares, what should be displayed, if a certain glyph is not found in the font, and if there are no fallback mechanisms. It also shows, how glyphs are created: By simply adding any graphical SVG content inside. You can use literally any other SVG elements in there, even {{ SVGElement("filter") }}, {{ SVGElement("a") }} or {{ SVGElement("script") }}. For simple glyphs, however, you can simply add a <code>d</code> attribute that works exactly like for paths.
 
The actual glyphs are then defined by {{ SVGElement("glyph") }} elements. The most important attribute is <code>unicode</code>. It defines the Unicode Codepoint, that is represented by this glyph. If you specify the <code>lang</code> attribute, you can furthermore restrict the glyph for certain languages (represented by <code>xml:lang</code> on the target) exclusively. Again, you can use arbitrary SVG to define the glyph, which allows for great effects in conforming user agents.
 
There are two further elements, that can be defined inside <code>font</code>, {{ SVGElement("hkern") }} and {{ SVGElement("vkern") }}. Each instance carries references to at least two characters and an attribute k that determines how much the distance between those characters should be decreased. The basic example are "A" and "V", where renderers should place "AV" much narrower than the single character definitions imply.

<pre>&lt;hkern u1="A" u2="V" k="20" /&gt;</pre>
 
== Referencing a font ==
 
This is a fairly simple one. If you have put together your font declaration as described above, you can just use a simple <code>font-family</code> attribute.
 
<pre>&lt;font&gt;
  &lt;font-face font-family="Super Sans" /&gt;
  &lt;!-- and so on --&gt;
&lt;/font&gt;

&lt;text font-family="Super Sans"&gt;My text uses Super Sans&lt;/text&gt;</pre>
 
However, you are free to combine several methods for great freedom of how and where to define the font.
 
=== Option: Use CSS @font-face ===
 
You can use @font-face to reference remote (and not so remote) fonts.
 
<pre>&lt;font id="Super_Sans"&gt;
  &lt;!-- and so on --&gt;
&lt;/font&gt;

&lt;style type="text/css"&gt;
@font-face {
  font-family: "Super Sans";
  src: url(#Super_Sans);
}
&lt;/style&gt;

&lt;text font-family="Super Sans"&gt;My text uses Super Sans&lt;/text&gt;</pre>
 
=== Option: reference a remote font ===
 
The above mentioned font-face-uri allows to reference an external font, hence allowing greater re-usability.
 
<pre>&lt;font&gt;
  &lt;font-face font-family="Super Sans"&gt;
    &lt;font-face-src&gt;
      &lt;font-face-uri xlink:href="fonts.svg#Super_Sans" /&gt;
    &lt;/font-face-src&gt;
  &lt;/font-face&gt;
&lt;/font&gt; </pre>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/SVG_fonts
|MSDN_link=
|HTML5Rocks_link=
}}