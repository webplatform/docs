{{Page_Title|SVG syntax and deployment}}
{{Flags
|State=In Progress
|Editorial notes=Fix multiple broken links
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article shows the basic syntax and usage of SVG.}}
{{Tutorial
|Content=== A Simple Example ==

Let us dive straight in with a simple example. Take a look at the following code.
 
<pre>&lt;svg version="1.1"
     baseProfile="full"
     xmlns="http://www.w3.org/2000/svg"&gt;

  &lt;rect width="100%" height="100%" fill="red" /&gt;

  &lt;circle cx="150" cy="100" r="80" fill="green" /&gt;

  &lt;text x="150" y="125" font-size="60" text-anchor="middle" fill="white"&gt;SVG&lt;/text&gt;

&lt;/svg&gt;</pre>
 
Copy the code and paste it in a file demo1.svg. Then open the file in Firefox. It will render as shown in the following screenshot. (Firefox users: click [[here]])
 
[[Image:=svgdemo1.png|svgdemo1.png]]

The rendering process involves the following:
 
# We start with the <code>svg</code> root element:
#* a doctype declaration as known from (X)HTML should be left off because DTD based SVG validation lead to more problems than it solves
#* to identify the version of the SVG for other types of validation the <code>version</code> and <code>baseProfile</code> attributes should always be used instead
#* as an XML dialect, SVG must always bind the namespaces correctly (in the xmlns attribute). See the [[Namespaces Crash Course]] page for more info.
#
# The background is set to red by drawing a rectangle [[<rect/>]] that covers the complete image area
# A green circle [[<circle/>]] with a radius of 80px is drawn atop the center of the red rectangle (offset 30+120px inward, and 50+50px upward).
# The text "SVG" is drawn. The interior of each letter is filled in with white. The text is positioned by setting an anchor at where we want the midpoint to be: in this case, the midpoint should correspond to the center of the green circle. Fine adjustments can be made to the font size and vertical position to ensure the final result is aesthetically pleasing.
 
=== Basic properties of SVG files ===
 
* The first important thing to notice is the order of rendering of elements. The globally valid rule for SVG files is, that ''later'' elements are rendered ''atop previous'' elements. The further down an element is the more will be visible.
* SVG files on the web can be displayed directly in the browser or embedded in HTML files via several methods:
** If the HTML is XHTML and is delivered as type <code>application/xhtml+xml</code>, the SVG can be directly embedded in the XML source.
** If the HTML is HTML5, and the browser is a conforming HTML5 browser, the SVG can be directly embedded, too. However, there may be syntax changes necessary to conform to the HTML5 specification
** The SVG file can be referenced with an <code>object</code> element:         <pre>         &lt;object data="image.svg" type="image/svg+xml" /&gt; </pre>
** Likewise an <code>iframe</code> element can be used:         <pre>         &lt;iframe src="image.svg"&gt;&lt;/iframe&gt; </pre>
** An <code>img</code> element can be used theoretically, too. However this technique doesn't work in Firefox before 4.0.
** Finally SVG can be created dynamically with JavaScript and injected into the HTML DOM. This has the advantage, that replacement technologies for browsers, that can't process SVG, can be implemented.
* See [[this dedicated article]] for an in-depth dealing with the topic.
* How SVG handles sizes and units will be explained [[on the next page]].
 
=== SVG File Types ===
 
SVG files come in two flavors. Normal SVG files are simple text files containing SVG markup. The recommended filename extension for these files is ".svg" (all lowercase).
 
Due to the potentially massive size SVG files can reach when used for some applications (e.g., geographical applications), the SVG specification also allows for gzip-compressed SVG files. The recommended filename extension for these files is ".svgz" (all lowercase). Unfortunately it is very problematic to get gzip-compressed SVG files to work reliably across all SVG capable user agents when served from Microsofts IIS server, and Firefox can not load gzip-compressed SVG from the local computer. Avoid gzip-compressed SVG except when you are publishing to a webserver that you know will serve it correctly. For normal SVG files, servers should send the <code>Content-Type: image/svg+xml</code> HTTP header. For gzip-compressed SVG files, servers should also send the <code>Content-Encoding: gzip</code> header.
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
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Getting_Started
|MSDN_link=
|HTML5Rocks_link=
}}