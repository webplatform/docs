{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A collection of rules in a document's stylesheet.}}
{{API_Object_Property
|Property_applies_to=css/cssom/styleSheet
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
This collection is always accessible, even if the style sheet is not enabled. Rules are added to the [[css/cssom/rules|'''rules''']] collection with the [[css/cssom/methods/addRule|'''addRule''']] method on the individual style sheet. A rule that is added to a [[html/attributes/disabled|'''disabled''']] style sheet does not apply to the document unless the style sheet is enabled. Rules are deleted with the [[css/cssom/methods/removeRule|'''removeRule''']] method.
The rules in this collection are in the source order of the document. As rules are added or deleted through the Cascading Style Sheets (CSS) Object Model, a rule's absolute position in the [[css/cssom/rules|'''rules''']] collection might change, but its position relative to other rules remains the same. When you add rules without specifying an index, the rule gets added to the document last. If you specify an index, however, the rule is inserted before the rule currently in that ordinal position in the collection. If the specified index is greater than the number of rules in the collection, the rule is added to the end.
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>styleSheet</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}