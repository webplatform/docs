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
|Property_applies_to=dom/Window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''status''' property to control a check box that is disabled by default.
|Code=&lt;INPUT ID{{=}}oCheckbox TYPE{{=}}checkbox CHECKED DISABLED&gt;
:
&lt;SPAN onclick{{=}}"oCheckbox.status{{=}}false" 
    STYLE{{=}}"font-weight:bold"&gt;I disagree&lt;/SPAN&gt;.
&lt;SPAN onclick{{=}}"oCheckbox.status{{=}}true" 
    STYLE{{=}}"font-weight:bold"&gt;I agree&lt;/SPAN&gt;.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/status.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''status''' property of the '''textArea''' object has a default value of null.
Setting the '''status''' property of a '''textArea''' object updates the value of the property and causes the [[dom/Element/propertychange|'''onpropertychange''']] event to fire. However, this change has no visual effect on the '''textArea''' object.
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