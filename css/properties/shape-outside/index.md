{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Declares a shape around which text should be wrapped, with possible modifications from the [[css/properties/shape-margin|shape-margin]] property. The shape defined by shape-outside and shape-margin changes the geometry of a float element's float area.}}
{{CSS Property
|Initial value=auto
|Applies to=Floats
|Inherited=No
|Media=visual
|Computed value=Computed lengths for <basic-shape>, the absolute URI for <image>, otherwise as specified.
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=The float area uses the margin box as normal.
}}{{CSS Property Value
|Data Type=<basic-shape>
|Description=The shape is computed based on the values of one of ''rectangle, inset-rectangle, circle, ellipse'' or ''polygon'':

* <code>rectangle(&lt;x&gt;, &lt;y&gt;, &lt;width&gt;, &lt;height&gt; [, &lt;rx&gt;, &lt;ry&gt;])</code> defines a rectangle with an origin and a size. The optional arguments '''rx''' and '''ry''' define the "rounded corners" in the horizontal and vertical direction.
* <code>inset-rectangle(&lt;top&gt;, &lt;right&gt;, &lt;bottom&gt;, &lt;left&gt; [, &lt;rx&gt;, &lt;ry&gt;])</code> defines a rectangle by top, right, bottom and left insets. The optional arguments '''rx''' and '''ry''' define the "rounded corners" in the horizontal and vertical direction.
* <code>circle(<cx, <cy>, <r>)</code> defines a circle with a center point and a radius.
* <code>ellipse(<cx, <cy>, <rx>, <ry>)</code> defines a circle with a center point and a radii for the horizontal and vertical directions.
* <code>polygon(<x1> <y1>, <x2> <y2>, ..., <xn> <yn>)</code> defines a polygon based on a list of points
}}{{CSS Property Value
|Data Type=<image>
|Description=If <image> references an image (fetched using the CORS-enabled fetch method defined by the HTML5 specification), the shape is extracted and computed based on the alpha channel of the image. If <image> does not reference an image or if the fetch attempt results in any error such that there is no fallback image, the effect is as if the value ''auto'' had been specified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* shape used is a rectangle equal to the content box */
shape-outside: rectangle(0, 0, 100%, 100%);

/* shape used is an inset rectangle 10px smaller than the content box in each dimension */
shape-outside: inset-rectangle(5px, 5px, 5px, 5px);

/* shape used is a rounded rectangle */
shape-outside: rectangle(0 ,0, 100%, 100%, 10px, 10px);

/* shape used is a circle filling the content box */
shape-outside: circle(0, 0, 50%);

/* shape used is an ellipse, wider than it is tall */
shape-outside: ellipse(0, 0, 50%, 30%);

/* shape used is a diamond, described as a polygon */
shape-outside: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);

/* shape used is the alpha channel of an image file */
shape-outside: url(path/to/image.png);
|LiveURL=http://code.webplatform.org/gist/5832982
}}
}}
{{Notes_Section
|Usage=Currently implemented as an experimental feature in WebKit and Blink. This can be used with a -webkit- prefix in WebKit nightly builds and with a -webkit- prefix in Chrome Canary builds with experimental-webkit-features enabled: chrome://flags/#enable-experimental-webkit-features
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://dev.w3.org/csswg/css-shapes/
|Status=Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=[[css/properties/shape-margin|shape-margin]]
[[css/properties/shape-image-threshold|shape-image-threshold]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}