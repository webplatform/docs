{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''hasLayout''' property to determine whether an object has layout.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/hasLayout.htm
|Code=
&lt;DIV ID{{=}}"oWidthSet" STYLE{{=}}"width:100%"&gt;
	DIV element A has its width set to 100%.&lt;/DIV&gt;
&lt;DIV ID{{=}}"oNotSet"&gt;DIV element B is not positioned, 
	and neither its height nor width is set.&lt;/DIV&gt;
&lt;P&gt;Which DIV element has layout?&lt;/P&gt;
&lt;BUTTON onclick{{=}}"alert(oWidthSet.currentStyle.hasLayout)"&gt;
	DIV Element A&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"alert(oNotSet.currentStyle.hasLayout)"&gt;
	DIV Element B&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The following table shows Cascading Style Sheets (CSS) properties and corresponding values that, if set, cause an element to have a layout.
{| class="wikitable"
|-
!CSS property
!Value
|-
|[[css/properties/display|'''display''']]
|'''inline-block'''
|-
|[[css/cssom/screen/height|'''height''']]
|any value
|-
|[[css/properties/float|'''styleFloat''']]
|'''left''' or '''right'''
|-
|[[css/properties/position|'''position''']]
|'''absolute'''
|-
|[[css/cssom/screen/width|'''width''']]
|any value
|-
|[[css/properties/writing-mode|'''writingMode''']]
|'''tb-rl'''
|-
|[[css/selectors/zoom|'''zoom''']]
|any value
|}
 
By setting the [[html/attributes/contentEditable|'''contentEditable''']] property to '''true''', you can cause an element to have a layout.
The following elements always have layout: '''body''', '''img''', '''HTMLInputElement''', [[html/elements/table|'''table''']] and '''td'''.
As of Microsoft Internet Explorer 6, when the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration specifies strict standards compliance, inline elements ignore the [[css/cssom/screen/width|'''width''']] property and the [[css/cssom/screen/height|'''height''']] property. By setting the '''width''' property and the '''height''' property, you cannot cause the element to have a layout.
|Import_Notes=
===Syntax===
<code>'''hasLayout: '''VARIANT_FALSE '''{{!}}''' VARIANT_FALSE</code>
===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows 2000 Server
|-
!Header
|<dl>
<dt>Mshtml.h</dt>
</dl>
|-
!IDL
|<dl>
<dt>Mshtml.idl</dt>
</dl>
|-
!DLL
|<dl>
<dt>Mshtml.dll</dt>
</dl>
|}

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}