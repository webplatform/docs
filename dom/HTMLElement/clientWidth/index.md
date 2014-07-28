{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=summary, examples best practices, compatibility, standards, clean-up of MSDN sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how the '''clientWidth''' property and the [[dom/HTMLElement/offsetWidth|'''offsetWidth''']] property measure document width differently. The width of the '''div''' is set to 200, and this is the value retrieved by the '''offsetWidth''' property, not the '''clientWidth''' property.
|Code=&lt;DIV ID{{=}}oDiv STYLE{{=}}"overflow:scroll; width:200; height:100"&gt; . . . &lt;/DIV&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.clientWidth)"&gt;client width&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.offsetWidth)"&gt;offset widthY&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientWidth.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}