{{Page_Title|overflow-x}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>overflow-x</code> property is a specific case of the generic <code>overflow</code> property. It controls how extra text exceeding the x axys of the bounding box of an element is rendered.}}
{{CSS Property
|Initial value=visible
|Applies to=non-replaced block-level elements and non-replaced ‘inline-block’ elements
|Inherited=No
|Media=visual
|Computed value=as specified, except ‘visible’
|Animatable=No
|Values={{CSS Property Value
|Data Type=visible
|Description=Default. Content is not clipped and scroll bars are not added. Elements are clipped to the size of the containing window or frame.
}}{{CSS Property Value
|Data Type=scroll
|Description=Content is clipped and scroll bars are added, even if the content does not exceed the dimensions of the object.
}}{{CSS Property Value
|Data Type=hidden
|Description=Content that exceeds the dimensions of the object is not shown.
}}{{CSS Property Value
|Data Type=auto
|Description=Content is clipped and scrolling is added only when necessary.
}}{{CSS Property Value
|Data Type=no-display
|Description=When the content doesn't fit in the content box, the whole box is removed, as if ‘display: none’ were specified.
}}{{CSS Property Value
|Data Type=no-content
|Description=When the content doesn't fit in the content box, the whole content is hidden, as if ‘visibility: hidden’ were specified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Using <code>overflow-x</code> width its values.

|Code=.hidden {
	overflow-x: hidden;
}
.scroll {
	overflow-x: scroll;
}
.auto {
	overflow-x: auto;
}
.visible {
	overflow-x: visible;
}

p {
	white-space: nowrap;
}

/* Set some default styles */
body {
	width: 20em;
	margin: 0 auto;
}
|LiveURL=http://code.webplatform.org/gist/6366308
}}
}}
{{Notes_Section
|Usage=The <code>overflow-y</code> CSS property specifies whether to clip content, render a scroll mechanism, or display overflow content of a block-level element, when it overflows at the top and bottom edges.
|Notes=Setting the overflow-y property to visible causes the content to clip to the size of the window or frame that contains the object.

Firefox has a vendor specific extension:

- <code>-moz-scrollbars-horizontal</code> – deprecated, use of overflow-x preferred.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model
|URL=http://dev.w3.org/csswg/css-box/#overflow-x
|Status=Editor's Draft
}}{{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/#overflow1
|Status=Working Draft
|Relevant_changes=Add no-display and no-content
}}{{Related Specification
|Name=CSS3 module: The box model
|URL=http://www.w3.org/TR/2002/WD-css3-box-20021024/
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-y
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}