{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Declares a shape around which text should be wrapped, with possible modifications from the [[css/properties/shape-margin|shape-margin]] property. The shape defined by shape-outside and shape-margin changes the geometry of a float element's float area.}}
{{CSS Property
|Initial value=none
|Applies to=Floats
|Inherited=No
|Media=visual
|Computed value=As defined for <basic-shape> (with <shape-box> following, if supplied), the <image> with its URI made absolute, otherwise as specified.
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=The float area is unaffected.
}}{{CSS Property Value
|Data Type=<basic-shape>
|Description=The shape is computed based on the values of one of ''inset, circle, ellipse'' or ''polygon''.  If shape-box is not supplied, then the reference box defaults to margin-box.

* <code>inset(&lt;shape-arg&gt;{1,4} [round&lt;border-radius&gt;])</code>. Defines an inset rectangle. The basic syntax for inset is the same as the margin shorthand syntax (see [[css/properties/margin|margin]] for details).  The optional border-radius argument  defines an inset's rounded corners using the border-radius shorthand syntax (see [[css/properties/border-radius|border-radius]] for details).

* <code>circle([&lt;shape-radius&gt;] [at &lt;position&gt;])</code> The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [[css/properties/background-position|background-position]] for details).

* <code>ellipse([&lt;shape-radius&gt;{2}] [at &lt;position&gt;])</code> The shape-radius argument is the radius of the circle. The position argument defines the center point of the circle and has the same syntax as background-position (see [[css/properties/background-position|background-position]] for details).

* <code>polygon([&lt;fill-rule&gt;,] [&lt;shape-arg&gt; &lt;shape-arg&gt;]# )</code> The fill-rule is used to determine the interior of the polygon (see the SVG [[svg/attributes/fill-rule|fill-rule]] for details). Each pair in the shape-arg represents x and y coordinates of each vertex in the polygon.
}}{{CSS Property Value
|Data Type=<shape-box>
|Description=The shape is defined by the CSS Box Model of the element the shape is applied to:

* <code>margin-box</code>
* <code>border-box</code>
* <code>padding-box</code>
* <code>content-box</code>
}}{{CSS Property Value
|Data Type=<image>
|Description=If <image> references an image (fetched using the CORS-enabled fetch method defined by the HTML5 specification), the shape is extracted and computed based on the alpha channel of the image as defined by [[css/properties/shape-image-threshold|shape-image-threshold]]. If <image> does not reference an image or if the fetch attempt results in any error such that there is no fallback image, the effect is as if the value ''auto'' had been specified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* shape used is a rectangle equal to the margin box */
shape-outside: inset(0 0 0 0);   
/* Or equivalent: */ 
shape-outside: inset(0);            
/* Or equivalent: */
shape-outside: margin-box;

/* shape used is an inset rectangle 10px smaller than the content box in each dimension */
shape-outside: inset(5px 5px 5px 5px);    
/* Or equivalent: */
shape-outside: inset(5px);                         

/* shape used is a rounded rectangle */
shape-outside: inset(0 round 20px) border-box; 
/* Or equivalent: */
border-radius: 20px;
-webkit-shape-outside: border-box;

/* shape used is a circle filling the content box */
shape-outside:  circle();       
/* Or equivalent: */
shape-outside:  circle() at center;     
/* Or equivalent: */
shape-outside:  circle(50%);     
/* Or equivalent: */
shape-outside:  circle(50% at center);  

/* shape used is an ellipse, wider than it is tall */
shape-outside:  ellipse(50% 30%);        
/* Or equivalent: */
shape-outside:  ellipse(50% 30% at center);

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