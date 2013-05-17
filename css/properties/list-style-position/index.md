{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies if the list-item markers should appear inside or outside the content flow.}}
{{CSS Property
|Initial value=outside
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=outside
|Description=Default. Marker is placed outside the text, and any wrapping text is not aligned under the marker.
}}{{CSS Property Value
|Data Type=inside
|Description=Marker is placed inside the text, and any wrapping text is aligned under the marker.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''list-style-position''' attribute and the '''list-style-position''' property to set the position for markers.

This example uses '''ul''' and <code>UL.compact</code> as selectors in an embedded (global) style sheet to set the position of the list-item markers.
|Code=UL	{ list-style-position:inside }
UL.compact { list-style-position:outside }
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-position.htm
}}{{Single Example
|Description=This example uses inline scripting to change the marker position when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;SPAN STYLE{{=}}"width:3cm" onmouseover{{=}}"this.style.listStylePosition{{=}}'inside'"
    onmouseout{{=}}"this.style.listStylePosition{{=}}'outside'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStylePosition.htm
}}{{Single Example
|Language=CSS
|Description=list-style-position example using both values
|Code=/*
	list-style-position example
	notice the difference based on the background color
	the &lt;li&gt; has a gray background to stand out
	the border represents the &lt;ul&gt;
*/

.list-position--outside {
	list-style-position: outside; /* this is also the default value */
}

.list-position--inside {
	list-style-position: inside;
}

/*
	Example for unordered lists
*/

.list-style--circle {
	list-style-type: circle;
}

.list-style--square {
	list-style-type: square;
}

li {
	background:#eee;
}

ul {
	border:1px solid #aaa;
}
|LiveURL=http://code.webplatform.org/gist/5597676
}}{{Single Example
|Language=CSS
|Description=Using list-style-position to display otherwise hidden list markers
|Code=/*
If the left padding is set to 0 the list-item markers do not show
This happens only if the list-style-position is set on outside (which is the default)
A ul contained in a div with overflow hidden might run into this issue
*/

ul {
	padding:0;
}

.list-position--inside {
	list-style-position: inside;
}
|LiveURL=http://code.webplatform.org/gist/5598129
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style-position''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]:'''list-item''' property is available starting with Microsoft Internet Explorer 6.
If the left padding of a list is set to 0 using one of the [[css/properties/padding|'''padding''']] properties, the list-item markers do not show only if that list has the default list-style-position: inside; . For a better understanding see the examples.
|Import_Notes====Syntax===
<code>'''list-style-position: '''inside '''{{!}}''' outside</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.5
}}
{{Related_Specifications_Section
|Specifications=
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
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}