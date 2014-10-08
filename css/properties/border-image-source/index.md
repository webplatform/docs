{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The property <code>border-image-source</code> is used to set the image to be used instead of the border style. If this is set to <code>none</code> the <code>border-style</code> is used instead.}}
{{CSS Property
|Initial value=none
|Applies to=all elements, except table elements where <code>border-collapse: collapse</code> is applied
|Inherited=No
|Media=visual
|Computed value=‘none’ or the image with its URI made absolute
|Animatable=No
|CSS object model property=borderImageSource
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. <code>border-style</code> is used instead.
}}{{CSS Property Value
|Data Type=url(path/to/image.png)
|Description=This value contains a path to an image that you want to apply to the element in question as a background image, using the CSS images syntax, as described at [[css/functions/url()|"CSS images: url()"]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing a &lt;div&gt; that has border-image-source property and other border-image properties.
|Code=&lt;div class="pattern"&gt;border-image&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5621011
}}{{Single Example
|Language=CSS
|Description=
|Code=/* General setup of the containers */
div {
	height: 100px;
	width: 100px;
	margin: 25px; 
	text-align: center;
	line-height: 100px;
	font-family: sans-serif;
}

/* This general class will apply the pattern to the containers */
.pattern {
	border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
	border-image-slice: 30;
	border-image-width: 6;
	border-image-outset: 3;	
}
|LiveURL=http://code.webplatform.org/gist/5621011
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Backgrounds and Borders Module
|URL=http://www.w3.org/TR/css3-background/#the-border-image-source
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_links=* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}