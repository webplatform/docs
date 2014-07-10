{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; update/improve example; update descriptions
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves whether the object can be transparent.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows four ways to use the '''allowTransparency''' attribute, with and without the [[css/properties/background-color|'''background-color''']] attribute. Because the '''allowTransparency''' attribute of Frame1 is set to '''true''', Frame1 renders red, the background color of the parent document.  The '''allowTransparency''' attribute of Frame2 is also set to '''true''', however the '''background-color''' attribute of Frame2 is set to <code>green</code>, so Frame2 renders green.  Because the '''allowTransparency''' attribute of Frame3 is set to '''false''' (the default value), Frame3 renders white, the color of the '''t:SRC''' document.  The '''allowTransparency''' attribute of Frame4 is also set to '''false''', so Frame4 renders white even though the '''background-color''' attribute of Frame4 is set to <code>green</code>.
|Code=&lt;BODY STYLE{{=}}"background-color: red"&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/allowTransparency.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
When the property is set to '''VARIANT_FALSE''', the [[css/properties/background-color|'''backgroundColor''']] property of the object can only be that of the window.  When the property is set to '''VARIANT_TRUE''', the '''backgroundColor''' property of the object can be set to any value, including the default value of '''transparent'''.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
Support for this attribute has been dropped in IE9.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=Beta
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=0.8
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=6
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=Beta
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=14
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=4
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=3
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=Beta
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}