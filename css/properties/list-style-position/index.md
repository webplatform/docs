{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
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
|Description=This example uses inline scripting to change the marker position to inside when an [[dom/events/mouseover|'''onmouseover''']] event occurs and revert the position to outside when an [[dom/events/mouseout|'''onmouseout''']] event occurs..
|Code=&lt;ul onMouseOver="this.style.listStylePosition='inside';" onMouseOut="this.style.listStylePosition='outside';"&gt;
|LiveURL=http://code.webplatform.org/gist/5841730
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
}}{{Single Example
|Language=HTML
|Description=Different behaviour with lists items containing block elements
|Code=&lt;ul>
	&lt;li&gt;List item&lt;/li&gt;
	&lt;li&gt;List item&lt;/li&gt;
	&lt;li&gt;&lt;h1&gt;Heading&lt;/h1&gt;&lt;/li&gt; &lt;!-- jumps to next line in some browsers --&gt;
	&lt;li&gt;List item&lt;/li&gt;
&lt;/ul&gt;
|LiveURL=http://code.webplatform.org/gist/5610773
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style-position''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]:'''list-item''' property is available starting with Microsoft Internet Explorer 6.

If the left padding of a list is set to 0 using one of the [[css/properties/padding|'''padding''']] properties, the list-item markers do not show only if that list has the default list-style-position: outside; . For a better understanding see the examples.

There is variance among browsers regarding behaviour when a block element is placed first within a list element declared as list-style-position:inside. Chrome and Safari both place this element on the same line as the marker box, whereas Firefox, Internet Explorer and Opera place it on the next line. There is also an example provided. [https://bugzilla.mozilla.org/show_bug.cgi?id{{=}}36854 Firefox bug report]
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