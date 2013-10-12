{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that sets the [[css/properties/list-style-type|<code>list-style-type</code>]], [[css/properties/list-style-position|<code>list-style-position</code>]] and [[css/properties/list-style-image|<code>list-style-image</code>]] properties in one declaration.}}
{{CSS Property
|Initial value=disc outside none
|Applies to=elements with display: list-item
|Inherited=Yes
|Media=visual
|Computed value=see individual properties
|Animatable=No
|CSS object model property=listStyle
|Values={{CSS Property Value
|Data Type=list-style-type list-style-position list-style-image
|Description=The <code>list-style</code> property can contain up to three components:
* <code>list-style-type</code>: This takes any of the range of style values available to the [[css/properties/list-style-type|'''list-style-type''']], which includes <code>circle</code>, <code>disc</code>, <code>decimal</code>, <code>upper-roman</code>, etc. To see a the full list of possible values, see the [[css/properties/list-style-type|'''list-style-type''']]. 
* <code>list-style-position</code>: Specifies if the list-item markers should appear inside or outside the content flow.
* <code>list-style-image</code>: This property sets the image that will be used as the list item marker.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent. (Acts similarly to other uses of inherit in CSS.)
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example contains multiple examples of using this property, omitting some of the values.
|Code=/* Specifying the list-style providing all the values */
.first-list {  
	list-style: disc inside url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);  
}  
 
 /* Omitting the position value it will use its default, 'outside' */
.second-list {  
 	list-style: disc url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg); 
}
 
  /* When an available image is provided, it always takes precedence over type */
.third-list {  
 	list-style: circle url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);  
}

/* When omitting image and type, it will use their default values: 'disc' for type and and 'none' for image*/
.fourth-list {  
 	list-style: outside;  
}
|LiveURL=http://code.webplatform.org/gist/6950114
}}{{Single Example
|Language=CSS
|Description=An example to show how setting padding-left to 0 when position is set to outside will produce the market not being shown at all. A ul contained in a div with overflow hidden might run into this issue.
|Code=ul {
	padding-left: 0;
}

.list-position-outside {
	list-style-position: outside;
}

.list-position-inside {
	list-style-position: inside;
}
|LiveURL=http://code.webplatform.org/gist/5598129
}}
}}
{{Notes_Section
|Usage=The <code>list-style</code> property is a composite property. You can omit one or more of the values. If both <code>list-style-type</code> and <code>list-style-image</code> are provided, and the value for this last one is different than '''none''' and links to an available image, the image takes precedence and it will be shown as the marker.

When the <code>list-style-position</code> value is set to '''outside''' and the [[css/properties/padding|'''padding''']] or [[css/properties/padding-left|'''padding-left''']] is set to 0, the list marker won't be displayed.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Lists and Counters Module Level 3
|URL=http://dev.w3.org/csswg/css3-lists/#list-style
|Status=Working Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/generate.html#propdef-list-style
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
|Opera_version=7.0
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
|Topic_clusters=Generated and Replaced Content
|Manual_sections====Related pages===
*<code>[[css/properties/list-style-type|'''list-style-type''']]</code>
*<code>[[css/properties/list-style-position|'''list-style-position''']]</code>
*<code>[[css/properties/list-style-image|'''list-style-image''']]</code>
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}