{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the width of the content area of an element. The content area of the element width does not include the [[css/properties/padding|padding]], [[css/properties/border|border]], and [[css/properties/margin|margin]] of the element.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements except inline, non-replaced elements, table rows, and row groups.
|Inherited=No
|Media=visual
|Computed value=percentage or absolute length
|Animatable=Yes
|CSS object model property=http://docs.webplatform.org/wiki/css/cssom/properties/width
|CSS percentages=refer to width of containing block
|Values={{CSS Property Value
|Data Type=auto
|Description=If auto is set for the elements width, the browser will determine the width for the element.
}}{{CSS Property Value
|Data Type=length
|Description=Will take a number that is immediately followed by a length unit such as px, em, in,  etc.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a %. The value is a percentage of the width of the parent object, whether or not it is specified explicitly.  Negative values are not allowed.
}}{{CSS Property Value
|Data Type=border-box
|Description=If border-box is used, the length or percentage defined will be applied to the element's border box.
}}{{CSS Property Value
|Data Type=content-box
|Description=If content-box is used, the length or percentage defined will be applied to the element's content-box.
}}{{CSS Property Value
|Data Type=max-content
|Description=The intrinsic preferred width
}}{{CSS Property Value
|Data Type=min-content
|Description=The intrinsic minimum width
}}{{CSS Property Value
|Data Type=available
|Description=The containing block width minus horizontal margin, border, and padding
}}{{CSS Property Value
|Data Type=fit-content
|Description=This will be either the large of the minimum width or the smaller of the preferred width and the available width
}}{{CSS Property Value
|Data Type=intrinsic
|Description=This is an experimental rule for max-content. Currently it only works in Chrome, however you should be using max-content instead since that is the standard.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=div { width: 100% }
h1 { width: 20em }
section { width: auto }
img { width: 100px }
}}{{Single Example
|Language=HTML
|Description=Example using new values that are part of the CSS Basic Box Model that is currently in working draft.
|Code=&lt;style&gt;
/* Width values of the CSS Box Model working draft */

div {
	box-sizing: border-box;
	border: 1px solid #444;
	width: 350px;
	margin: 5px;
}

p {
	background: #000;
	color: #fff;
	padding: 5px;
	font-family: Arial, sans-serif;
}

p.mincontent {
	/* vendor prefix needed */
	width: -webkit-min-content;
}

p.maxcontent {
	/* vendor prefix needed */
	width: -webkit-max-content;
} 

p.fitcontent {
	/* vendor prefix needed */
	width: -webkit-fit-content;
}
&lt;/style&gt;

&lt;div&gt;
&lt;p&gt;This is the content inside of the parent div.&lt;/p&gt;
&lt;/div&gt;

&lt;div&gt;
&lt;p class="mincontent"&gt;This is the content inside of the parent div.&lt;/p&gt;
&lt;p class="mincontent"&gt;Min-content matches the widest single word like "Antidisestablishmentarianism".&lt;/p&gt;
&lt;/div&gt;

&lt;div&gt;
&lt;p class="maxcontent"&gt;This is the content inside of the parent div. Max-content expands to fit the content.&lt;/p&gt;
&lt;/div&gt;

&lt;div&gt;
&lt;p class="fitcontent"&gt;This fits the content inside of the parent div.&lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5702862
}}
}}
{{Notes_Section
|Usage====Newer Values===
In the CSS Basic Box Model Working Draft, the values max-content, min-content, available, fit-content, border-box, and content-box were added. It would be a best practice to add the vendor prefix to these until the values are standardized.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic Box Model
|URL=http://dev.w3.org/csswg/css-box/#the-width-and-height-properties
|Status=Working Draft
|Relevant_changes=Keywords max-content, min-content, fit-content, border-box, and content-box added
}}{{Related Specification
|Name=CSS Level 2
|URL=http://www.w3.org/TR/CSS2/visudet.html#the-width-property
|Status=Recommendation
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#width
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Box Model, CSS Attributes
|External_links=* http://www.w3.org/TR/CSS2/visudet.html#the-width-property
* http://www.w3.org/TR/CSS21/visudet.html#propdef-width
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/width
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}