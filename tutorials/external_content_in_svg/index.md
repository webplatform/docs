{{Page_Title|External content in SVG}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article covers using external content inside SVG images, such as external image files, and XML data.}}
{{Tutorial
|Content=Apart from graphic primitives like rectangles and circles, SVG offers a set of elements to embed other types of content in images as well.
 
=== Embedding raster images ===
 
Much like the img element in HTML SVG has an <code>image</code> element to serve the same purpose. You can use it to embed arbitrary raster (and vector) images. The specification requests applications to support at least PNG, JPEG and SVG format files.
 
The embedded picture becomes a normal SVG element. This means, that you can use clips, masks, filters, rotations and all other tools of SVG on the content:

<pre>&lt;svg version="1.1"
     xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
     width="200" height="200"&gt;
  &lt;image x="90" y="-65" width="128" height="146" transform="'''rotate(45)'''"
     xlink:href="https://developer.mozilla.org/media/img/mdn-logo.png"/&gt;
&lt;/svg&gt;</pre>
 
[[Image:imagedemo.png]]
 
=== Embedding arbitrary XML ===
 
Since SVG is an XML application, you can of course ''always'' embed arbitrary XML anywhere in an SVG document. But then you have no means to define how the surrounding SVG should react on the content. Actually, in a conforming viewer it will react in no way at all, the data will simply be omitted. Therefore the specification adds the <code>{{ SVGElement("foreignObject") }}</code> element to SVG. Its sole purpose is to be a container for other markup and a carrier for SVG styling attributes (most prominently <code>width</code> and <code>height</code> to define the space the object will take).

The <code>foreignObject</code> element is a good way to embed XHTML in SVG. If you have longer texts, the HTML layout is more suitable and comfortable than the SVG <code>text</code> element. Another often cited use case is the embedding of formulas with MathML. For scientific applications of SVG this is a very good way to join both worlds.

  '''Note:''' Please keep in mind, that the content of the <code>foreignObject</code> must be processable by the viewer. A standalone SVG viewer is unlikely to be able to render HTML or MathML. 
Since the <code>foreignObject</code> is an SVG element, you can, like in the case of <code>image</code>, use any SVG goodness with it, which then will be applied to its content.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Other_content_in_SVG
|MSDN_link=
|HTML5Rocks_link=
}}