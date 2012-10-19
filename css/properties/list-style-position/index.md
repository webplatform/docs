{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
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
|Code=&lt;STYLE&gt;
    UL	{ list-style-position:inside }
    UL.compact { list-style-position:outside }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;UL&gt;
    &lt;LI&gt;... 
    &lt;LI&gt;... 
&lt;/UL&gt;
&lt;UL CLASS{{=}}compact&gt;
    &lt;LI&gt;... 
    &lt;LI&gt;...
&lt;/UL&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-position.htm
}}{{Single Example
|Description=This example uses inline scripting to change the marker position when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;SPAN STYLE{{=}}"width:3cm" onmouseover{{=}}"this.style.listStylePosition{{=}}'inside'"
    onmouseout{{=}}"this.style.listStylePosition{{=}}'outside'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStylePosition.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style-position''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]:'''list-item''' property is available starting with Microsoft Internet Explorer 6.
If the left margin of a list item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show. The margin should be set to a minimum of 30 points.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}