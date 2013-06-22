{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the height of an element. The content area of the element height does not include the [[css/properties/padding|padding]], [[css/properties/border|border]], and [[css/properties/margin|margin]] of the element.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=percentage or absolute height
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=If auto is set for the elements height, the browser will determine the height for the element.
}}{{CSS Property Value
|Data Type=height
|Description=Will take a number that is immediately followed by a length unit such as px, em, in,  etc.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer followed by a percent sign (%). The value is a percentage of the height of the parent object, which must be specified explicitly.  Negative values are not allowed.
}}{{CSS Property Value
|Data Type=border-box
|Description=If border-box is used, the height or percentage defined will be applied to the element's border box.
}}{{CSS Property Value
|Data Type=content-box
|Description=If content-box is used, the height or percentage defined will be applied to the element's content-box.
}}{{CSS Property Value
|Data Type=max-content
|Description=The intrinsic preferred height
}}{{CSS Property Value
|Data Type=min-content
|Description=The intrinsic minimum height
}}{{CSS Property Value
|Data Type=available
|Description=The containing block height minus horizontal margin, border, and padding
}}{{CSS Property Value
|Data Type=fit-content
|Description=This will be either the large of the minimum height or the smaller of the preferred height and the available height
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Height of div equal to 100% of the bounding element */
div { height: 100% }

/* Height of h1 equal to 20em */
h1 { height: 20em }

/* Height set to auto */
section { height: auto }

/* Height of image set to 100px */
img { height: 100px }
}}{{Single Example
|Language=HTML
|Description=Example using new values that are part of the CSS Basic Box Model that is currently in working draft.
|Code=&lt;style&gt;
/**
 * Height values of the CSS Box Model working draft
 */

div {
	box-sizing: border-box;
	border: 1px solid #444;
	margin: 5px;
	width: 250px;
}

p {
	background: #000;
	color: lightgrey;
	padding: 5px;
	font-family: Arial, sans-serif;
}

p.height200 {
	/* vendor prefix needed */
	height: 200px;
	background: blue;
	color: orange;
}

p.height25 {
	/* vendor prefix needed */
	height: 50px;
	background: red;
} 

p.height25solved {
	/* vendor prefix needed */
	height: 50px;
	background: green;
	overflow: hidden;
} 
&lt;/style&gt;
&lt;div&gt;
&lt;p&gt;This is the content inside of the parent div. Height is not set, so the height is defaulting to auto.&lt;/p&gt;
&lt;/div&gt;

&lt;div&gt;
&lt;p class="height200"&gt;This is the content inside of the parent div. It's height is set to 200px&lt;/p&gt;
&lt;/div&gt;

&lt;!-- You can solve the issue below by setting the overflow property --&gt;
&lt;div&gt;
&lt;p class="height25"&gt;This is the content inside of the parent div. The content extends beyond the bounding element and extends into elements below, interupting the flow.&lt;/p&gt;
&lt;/div&gt;

&lt;!-- Solved by setting the overflow property to hidden --&gt;
&lt;div&gt;
&lt;p class="height25solved"&gt;This is the content inside of the parent div. The content extends beyond the bounding element and extends into elements below, interupting the flow.&lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5702862
}}
}}
{{Notes_Section
|Notes====Remarks===
If you specify the '''height''' property of an '''img''' object but not the [[css/properties/width|'''width''']] property, the width is proportional to the height according to the dimensions of the image source file.
To perform operations on the numeric value of this property, use [[css/cssom/properties/pixelHeight|'''pixelHeight''']] or [[css/cssom/properties/posHeight|'''posHeight''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic Box Model
|URL=http://dev.w3.org/csswg/css-box/#the-width-and-height-properties
|Status=Working Draft
|Relevant_changes=Keywords max-content, min-content, fit-content, border-box, and content-box added
}}{{Related Specification
|Name=CSS Level 2
|URL=http://www.w3.org/TR/CSS2/visudet.html#the-height-property
|Status=Recommendation
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#height
|Status=Recommendation
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
|Topic_clusters=CSS Layout, Box Model, CSS Attributes, Grid Layout
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>Measuring Element Dimension and Location with CSSOM in Internet Explorer 9</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}