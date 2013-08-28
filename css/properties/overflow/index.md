{{Page_Title|overflow}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The overflow property controls how extra content exceeding the bounding box of an element is rendered. It can be used in conjunction with an element that has a fixed width and height, to eliminate text-induced page distortion.}}
{{CSS Property
|Applies to=non-replaced block-level elements and non-replaced ’inline-block’ elements
|Inherited=No
|Media=visual
|Computed value=as specified, except ‘visible’
|Animatable=No
|Values={{CSS Property Value
|Data Type=visible
|Description=Mostly the default value. Content is not clipped and a scroll mechanism is not added.
}}{{CSS Property Value
|Data Type=scroll
|Description=Content is clipped and a scroll mechanism is added, even if the content does not exceed the dimensions of the object.
}}{{CSS Property Value
|Data Type=hidden
|Description=Content that exceeds the dimensions of the object is not shown. No scroll mechanism is applied.
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
|Description=Add different behavior for paragraphs via the <code>overflow</code> property.
|Code=.hidden {
	overflow: hidden;
}
.scroll {
	overflow: scroll;
}
.auto {
	overflow: auto;
}
.visible {
	overflow: visible;
}

/* Helper for paragraphes */
p {
	height: 60px;
}
|LiveURL=http://code.webplatform.org/gist/6365118
}}
}}
{{Notes_Section
|Notes=The default value for the <code>html</code> element is <code>auto</code>.
Setting the <code>overflow</code> property to <code>visible</code> causes the content to clip to the size of the window or frame that contains the object.

Firefox has several vendor specific extensions:
- <code>-moz-scrollbars-none</code> – obsolete, use <code>overflow: hidden</code> instead.
- <code>-moz-scrollbars-horizontal</code> and <code>-moz-scrollbars-vertical</code> – deprecated, use of <code>overflow-x</code> and <code>overflow-y</code> is preferred.
- <code>-moz-hidden-unscrollable</code> non-standard, is intended mainly for internal use and by themes. Disables scrolling of XML root elements and <html>, <body> by arrow keys and mouse wheel.
|Import_Notes=*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 11.1.1
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=http://www.w3.org/TR/css3-box/#overflow1
|URL=CSS basic box model
|Status=Working Draft
|Relevant_changes=Add no-display and no-content
}}{{Related Specification
|Name=http://www.w3.org/TR/2002/WD-css3-box-20021024/
|URL=CSS3 module: The box model
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
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}