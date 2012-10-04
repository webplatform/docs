{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows four ways to use the '''allowTransparency''' attribute, with and without the [[css/properties/background-color|'''background-color''']] attribute. Because the '''allowTransparency''' attribute of Frame1 is set to '''true''', Frame1 renders red, the background color of the parent document.  The '''allowTransparency''' attribute of Frame2 is also set to '''true''', however the '''background-color''' attribute of Frame2 is set to <code>green</code>, so Frame2 renders green.  Because the '''allowTransparency''' attribute of Frame3 is set to '''false''' (the default value), Frame3 renders white, the color of the '''t:SRC''' document.  The '''allowTransparency''' attribute of Frame4 is also set to '''false''', so Frame4 renders white even though the '''background-color''' attribute of Frame4 is set to <code>green</code>.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/allowTransparency.htm
|Code=
&lt;BODY STYLE{{=}}"background-color: red"&gt;
&lt;IFRAME ID{{=}}"Frame1" SRC{{=}}"transparentBody.htm" allowTransparency{{=}}"true"&gt;
&lt;/IFRAME&gt;
&lt;IFRAME ID{{=}}"Frame2" SRC{{=}}"transparentBody.htm" allowTransparency{{=}}"true"
  STYLE{{=}}"background-color: green"&gt;
&lt;/IFRAME&gt;
&lt;IFRAME ID{{=}}"Frame3" SRC{{=}}"transparentBody.htm"&gt;
&lt;/IFRAME&gt;
&lt;IFRAME ID{{=}}"Frame4" SRC{{=}}"transparentBody.htm"
  STYLE{{=}}"background-color: green"&gt;
&lt;/IFRAME&gt;				
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When the property is set to '''VARIANT_FALSE''', the [[css/properties/background-color|'''backgroundColor''']] property of the object can only be that of the window.  When the property is set to '''VARIANT_TRUE''', the '''backgroundColor''' property of the object can be set to any value, including the default value of '''transparent'''.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}