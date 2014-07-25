{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=index
|Data type=any
|Description='''Integer''' that specifies the zero-based position of the cell to remove from the table row. If no value is provided, the last cell in the '''cells''' collection is deleted.
|Optional=No
}}
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''deleteCell''' method to delete the last cell in the first row of the table.
|Code=document.all.myTable.rows[0].deleteCell()
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
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