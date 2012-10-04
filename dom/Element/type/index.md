{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the [[apis/file/properties/type|'''type''']] property to create an alert that indicates the type of object selected by the user. If the user clicks the mouse pointer on the text "Some text", the alert reads "Text". If the user clicks the mouse pointer on the space to the right of the text, the alert reads "None".
|LiveURL=
|Code=
&lt;BODY onclick{{=}}"alert(document.selection.type)"&gt;
Some text.
}}}}
{{Notes_Section
|Notes=
===Remarks===
[[dom/selection|'''selection''']] is a child object of the [[dom/document|'''document''']] object.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/selection|selection]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}