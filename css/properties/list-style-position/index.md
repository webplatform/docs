{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies if the list-item markers should appear inside or outside the content flow.}}
{{CSS Property
|Initial value=outside
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=listStylePosition
|Values={{CSS Property Value
|Data Type=outside
|Description=Default. Marker is placed outside the list item, and any wrapping text is not aligned under the marker.
}}{{CSS Property Value
|Data Type=inside
|Description=Marker is placed inside the text, and any wrapping text is aligned under the marker.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.  (Acts similarly to other uses of inherit in CSS.)
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the '''list-style-position''' attribute and the '''list-style-position''' property to set the position for markers.

This example uses '''ul''' and <code>UL.compact</code> as selectors in an embedded (global) style sheet to set the position of the list-item markers.
|Code=.firstlist { list-style-position:inside }
.secondlist { list-style-position:outside }
|LiveURL=http://code.webplatform.org/gist/5841706
}}{{Single Example
|Language=JavaScript
|Description=This example shows how to change the value dynamically using JavaScript. The value changes from outside to inside when the mouse is over the list
|Code=var ul = document.getElementById('list-hover');

// When the mouse is over the list, the position changes to inside
ul.addEventListener('mouseover', function () {
	ul.style.listStylePosition = 'inside';
});

// When the mouse is not longer over the list, we revert back the value to outside
ul.addEventListener('mouseout', function () {
	ul.style.listStylePosition = 'outside';
});
|LiveURL=http://code.webplatform.org/gist/6949116
}}{{Single Example
|Language=CSS
|Description=An example to show how set padding to 0 when position is set to outside will produce the market not being shown at all. A ul contained in a div with overflow hidden might run into this issue.
|Code=ul {
	padding: 0;
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
|Usage====Remarks===
If a list-style-position is set to outside and padding-left is set to 0, the marker will not show.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS21/generate.html#propdef-list-style-position
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
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Attributes
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
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}