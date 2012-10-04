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
|Values={{CSS_Property_Value|Data Type=disc |Description=Default. Solid circles.}}
{{CSS_Property_Value|Data Type=circle |Description=Outlined circles.}}
{{CSS_Property_Value|Data Type=square |Description=Solid squares.}}
{{CSS_Property_Value|Data Type=decimal |Description=1, 2, 3, 4, and so on.}}
{{CSS_Property_Value|Data Type=decimal-leading-zero |Description=01, 02, 03, 04, and so on.}}
{{CSS_Property_Value|Data Type=lower-alpha |Description=A, b, c, d, and so on.}}
{{CSS_Property_Value|Data Type=upper-alpha |Description=A, B, C, D, and so on.}}
{{CSS_Property_Value|Data Type=lower-roman |Description=I, ii, iii, iv, and so on.}}
{{CSS_Property_Value|Data Type=upper-roman |Description=I, II, III, IV, and so on.}}
{{CSS_Property_Value|Data Type=lower-greek |Description=Lowercase classical Greek: alpha, beta, gamma, and so on.}}
{{CSS_Property_Value|Data Type=lower-latin |Description=A, b, c, d, and so on.}}
{{CSS_Property_Value|Data Type=upper-latin |Description=A, B, C, D, and so on.}}
{{CSS_Property_Value|Data Type=armenian |Description=Traditional Armenian numbering.}}
{{CSS_Property_Value|Data Type=georgian |Description=Traditional Georgian numbering: an, ban, gan, don, and so on.}}
{{CSS_Property_Value|Data Type=none |Description=No marker is shown.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''list-style-type''' attribute and the '''list-style-type''' property to set the markers.

This example uses '''ul''' as a selector in an embedded (global) style sheet to change the marker type to '''circle'''.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type.htm
|Code=
&lt;style&gt;
    ul { list-style-type:circle }
&lt;/style&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the marker type on when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyleType.htm
|Code=
&lt;UL onmouseover{{=}}"this.style.listStyleType{{=}}'circle'"&gt;
}}
{{Single_Example
|Description=This example demonstrates the newer line-item markers added for Internet Explorer 8.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type_ie8.htm
|Code=
&lt;style type{{=}}"text/css"&gt;
.decleadzero {
	list-style-type: decimal-leading-zero;
}
...
&lt;/style&gt;
&lt;body&gt;
 &lt;ol class{{=}}"decleadzero"&gt;
  &lt;li&gt;This is the first item. &lt;/li&gt;
  &lt;li&gt;This is the second item. &lt;/li&gt;
  &lt;li&gt;This is the third item. &lt;/li&gt;
 &lt;/ol&gt;
    ...
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''list-style-type''' property determines the appearance of the list-item marker if the value of the [[css/properties/list-style-image|'''list-style-image''']] attribute is set to '''none''', or if the image pointed to by the URL cannot be displayed.
The '''list-style-type''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]:'''list-item''' property is available starting with Microsoft Internet Explorer 6.
If the left margin of a line item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show. The margin should be set to a minimum of 30 points.
|Import_Notes=
===Syntax===
<code>'''list-style-type: '''disc '''{{!}}''' circle '''{{!}}''' square '''{{!}}''' decimal '''{{!}}''' decimal-leading-zero '''{{!}}''' lower-roman '''{{!}}''' upper-roman '''{{!}}''' lower-greek '''{{!}}''' lower-latin '''{{!}}''' upper-latin '''{{!}}''' armenian '''{{!}}''' georgian '''{{!}}''' lower-alpha '''{{!}}''' upper-alpha '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.3


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