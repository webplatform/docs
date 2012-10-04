{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''status''' property to control a check box that is disabled by default.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/status.htm
|Code=
&lt;INPUT ID{{=}}oCheckbox TYPE{{=}}checkbox CHECKED DISABLED&gt;
:
&lt;SPAN onclick{{=}}"oCheckbox.status{{=}}false" 
    STYLE{{=}}"font-weight:bold"&gt;I disagree&lt;/SPAN&gt;.
&lt;SPAN onclick{{=}}"oCheckbox.status{{=}}true" 
    STYLE{{=}}"font-weight:bold"&gt;I agree&lt;/SPAN&gt;.
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''status''' property of the '''textArea''' object has a default value of null.
Setting the '''status''' property of a '''textArea''' object updates the value of the property and causes the [[dom/events/propertychange|'''onpropertychange''']] event to fire. However, this change has no visual effect on the '''textArea''' object.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}radio</code>
*<code>textArea</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}