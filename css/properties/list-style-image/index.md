{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Replaces the list-item marker with an image.}}
{{CSS Property
|Initial value=none
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Computed value=absolute URI or 'none'
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. No image is specified.
}}{{CSS Property Value
|Data Type=url(path/to/image.png)
|Description=Location of the image, where path/to/image.png is an absolute or relative URL.  More details can be found at the [[css/functions/url()]] section.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the `list-style-image` property to modify the list item marker of an unordered list, specifying an absolute and a relative URL respectively.

This example uses '''ul''' as a selector in an embedded (global) style sheet to set the marker to the dot.gif image.
|Code=/* Using an absolute URI to specify an image */
.firstlist {
	list-style-image: url(http://docs.webplatform.org/static/images/logo.png);
} 

/* Using a relative URI to specify an image */
.secondlist {
	list-style-image: url(special_icon.png);
}
|LiveURL=http://code.webplatform.org/gist/5841596
}}{{Single Example
|Language=JavaScript
|Description=This example uses inline scripting to change the style of the list-item marker to an image when an [[dom/events/mouseover|'''onmouseover''']] event occurs.

Additionally, when an [[dom/events/mouseout|'''onmouseout''']] event occurs, `list-style-type` is set to "none", setting it back to the browser's default.
|Code=&lt;ul onMouseOver="this.style.listStyleImage='url(favicon.ico)';" onMouseOut="this.style.listStyleImage='none';"&gt;
|LiveURL=http://code.webplatform.org/gist/5841611
}}
}}
{{Notes_Section
|Usage=The property has limited positioning options for the background image, and in some circumstances doesn’t work at all in IE. 
So it has become a far more common practice to simply set a background image on the list items.
|Notes====Remarks===
When the image is available, it replaces the marker that is set with the [[css/properties/list-style-type|'''list-style-type''']] marker.
If the left margin of the list item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Lists and Counters Module Level 3
|URL=http://dev.w3.org/csswg/css3-lists/#list-style-image
|Status=Working Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/generate.html#propdef-list-style-image
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
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/list-style-image
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}