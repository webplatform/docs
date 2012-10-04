{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=VARIANT_TRUE |Description=Apply the line-through.}}
{{CSS_Property_Value|Data Type=VARIANT_FALSE |Description=Prevent the line-through.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''textDecorationLineThrough''' property to draw a line through the text when the user clicks it with the mouse.
|LiveURL=
|Code=
&lt;P onclick{{=}}"this.style.textDecorationLineThrough{{=}}true;"&gt;
Click this if you think it's unimportant.
&lt;/P&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''textDecorationLineThrough: '''VARIANT_TRUE '''{{!}}''' VARIANT_FALSE</code>
===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows Server 2003
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
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/text-decoration|textDecoration]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}