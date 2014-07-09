{{Page_Title}}
{{Flags
|State=Out of Date
|Editorial notes=I think the empty method only applies to the selection object, not a node collection.
this is legacy MSIE method of document.selection(); and does not apply to document Nodes.
MSDN doco ref: http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Cancels the current selection, sets the selection type to none, and sets the item property to null. }}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Node
|Example_object_name=selection
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
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
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Selection|Selection]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx empty() Method]
|HTML5Rocks_link=
}}