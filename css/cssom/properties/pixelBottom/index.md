{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary and more explanation needed.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/cssom/properties
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''pixelBottom''' property to set a positioned '''div''' to the bottom of the client area.
|Code=oDiv.style.pixelBottom {{=}} 0;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''pixelBottom''' property reflects the value of the Cascading Style Sheets (CSS) [[css/properties/bottom|'''bottom''']] attribute.
Unlike the [[css/properties/bottom|'''bottom''']] property, the '''pixelBottom''' value is an integer, not a string, and is always interpreted in pixels.
For more information about how to access the dimension and location of an object on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
<code>'''pixelBottom: '''''
&lt;integer&gt;
''</code>
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
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultSelected]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/properties/posBottom|posBottom]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}