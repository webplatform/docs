{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=none |Description=Default. No image is specified.}}
{{CSS_Property_Value|Data Type=url(sURL) |Description=Location of the image, where sURL is an absolute or relative URL.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''list-style-image''' attribute and the '''list-style-image''' property to set the image for markers.

This example uses '''ul''' as a selector in an embedded (global) style sheet to set the marker to the dot.gif image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-image.htm
|Code=
&lt;STYLE&gt;
    UL { list-style-image:url(dot.gif) }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the style of the list-item marker to an image when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyleImage.htm
|Code=
&lt;UL onmouseover{{=}}"this.style.listStyleImage{{=}}'url(dot.gif)'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''list-style-image''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]: '''list-item''' property is available starting with Microsoft Internet Explorer 6.
When the image is available, it replaces the marker that is set with the [[css/properties/list-style-type|'''list-style-type''']] marker.
If the left margin of the list item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show. The margin should be set to a minimum of 30 points.
|Import_Notes=
===Syntax===
<code>'''list-style-image: '''url(sURL) '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Generated and Replaced Content
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}