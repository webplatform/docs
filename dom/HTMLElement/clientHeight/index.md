{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
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
|Description=This example shows how the '''clientHeight''' property and the [[dom/HTMLElement/offsetHeight|'''offsetHeight''']] property measure document height differently. The height of the '''div''' is set to 100, and this is the value retrieved by the '''offsetHeight''' property, not the '''clientHeight''' property.
|Code=&lt;div id{{=}}"oDiv" style{{=}}"overflow: scroll; width: 200px; height: 100px"&gt;
    . . . &lt;/div&gt;
&lt;button onclick{{=}}"alert(oDiv.clientHeight)"&gt;client height&lt;/button&gt;
&lt;button onclick{{=}}"alert(oDiv.offsetHeight)"&gt;offset heightY&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientHeight.htm
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