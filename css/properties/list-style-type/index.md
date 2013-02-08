{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the type of list-item marker in a list.}}
{{CSS Property
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=armenian	
|Description=The marker is traditional Armenian numbering 
}}{{CSS Property Value
|Data Type=circle	
|Description=circle 
}}{{CSS Property Value
|Data Type=cjk-ideographic	
|Description=plain ideographic numbers 
}}{{CSS Property Value
|Data Type=decimal	
|Description= number. This is default for &lt;ol&gt; 
}}{{CSS Property Value
|Data Type=decimal-leading-zero	
|Description=number with leading zeros (01, 02, 03, etc.) 
}}{{CSS Property Value
|Data Type=disc	
|Description=filled circle. This is default for &lt;ul&gt;
}}{{CSS Property Value
|Data Type=georgian	
|Description=traditional Georgian numbering 
}}{{CSS Property Value
|Data Type=hebrew	
|Description=The marker is traditional Hebrew numbering 
}}{{CSS Property Value
|Data Type=hiragana	
|Description=traditional Hiragana numbering 
}}{{CSS Property Value
|Data Type=hiragana-iroha	
|Description= traditional Hiragana iroha numbering 
}}{{CSS Property Value
|Data Type=inherit	
|Description=The value of the listStyleType property is inherited from parent element	
}}{{CSS Property Value
|Data Type=katakana	
|Description=traditional Katakana numbering 
}}{{CSS Property Value
|Data Type=katakana-iroha	
|Description=traditional Katakana iroha numbering 
}}{{CSS Property Value
|Data Type=lower-alpha	
|Description=lower-alpha (a, b, c, d, e, etc.) 
}}{{CSS Property Value
|Data Type=lower-greek	
|Description=lower-greek 
}}{{CSS Property Value
|Data Type=lower-latin	
|Description=lower-latin (a, b, c, d, e, etc.) 
}}{{CSS Property Value
|Data Type=lower-roman	
|Description=lower-roman (i, ii, iii, iv, v, etc.) 
}}{{CSS Property Value
|Data Type=none	
|Description=No marker is shown 
}}{{CSS Property Value
|Data Type=square	
|Description=square 
}}{{CSS Property Value
|Data Type=upper-alpha	
|Description=upper-alpha (A, B, C, D, E, etc.)  
}}{{CSS Property Value
|Data Type=upper-latin	
|Description=upper-latin (A, B, C, D, E, etc.) 
}}{{CSS Property Value
|Data Type=upper-roman	
|Description=upper-roman (I, II, III, IV, V, etc.)
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''list-style-type''' attribute and the '''list-style-type''' property to set the markers.

This example uses '''ul''' as a selector in an embedded (global) style sheet to change the marker type to '''circle'''.
|Code=&lt;style&gt;
    ul { list-style-type:circle }
&lt;/style&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type.htm
}}{{Single Example
|Description=This example uses inline scripting to change the marker type on when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;UL onmouseover{{=}}"this.style.listStyleType{{=}}'circle'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/listStyleType.htm
}}{{Single Example
|Description=This example demonstrates the newer line-item markers added for Internet Explorer 8.
|Code=&lt;style type{{=}}"text/css"&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type_ie8.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style-type''' property determines the appearance of the list-item marker if the value of the [[css/properties/list-style-image|'''list-style-image''']] attribute is set to '''none''', or if the image pointed to by the URL cannot be displayed.
The '''list-style-type''' property can be applied to any element when [[css/properties/margin|'''margin''']] and [[css/properties/display|'''display''']]:'''list-item''' are applied. The [[css/properties/display|'''display''']]:'''list-item''' property is available starting with Microsoft Internet Explorer 6.
If the left margin of a line item is set to 0 using one of the [[css/properties/margin|'''margin''']] properties, the list-item markers do not show. The margin should be set to a minimum of 30 points.

===Browser Support===
The list-style-type property is supported in all major browsers.

Note: IE9 and Opera 11 do not support: cjk-ideographic, hebrew, hiragana, hiragana-iroha, katakana, and katakana-iroha.

Note: IE8, and earlier, only support the property values: decimal-leading-zero, lower-greek, lower-latin, upper-latin, armenian, georgian, and inherit if a DOCTYPE is specified!
|Import_Notes====Syntax===
<code>'''list-style-type: '''disc '''{{!}}''' circle '''{{!}}''' square '''{{!}}''' decimal '''{{!}}''' decimal-leading-zero '''{{!}}''' lower-roman '''{{!}}''' upper-roman '''{{!}}''' lower-greek '''{{!}}''' lower-latin '''{{!}}''' upper-latin '''{{!}}''' armenian '''{{!}}''' georgian '''{{!}}''' lower-alpha '''{{!}}''' upper-alpha '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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