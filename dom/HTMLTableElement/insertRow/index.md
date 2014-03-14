{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=index
|Data type=any
|Description='''Integer''' that specifies where to insert the row in the '''rows''' collection. The default value is '''-1''', which appends the new row to the end of the '''rows''' collection.
|Optional=No
}}
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

'''tr'''

null
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''insertRow''' method to add a row to the [[html/elements/table|'''table''']].
|Code=myNewRow {{=}} document.all.myTable.insertRow()
}}
}}
{{Notes_Section
|Notes====Remarks===
The preferred technique for inserting a row is to add the row at the end of the '''rows''' collection. It is faster to add a row at the end of a table than somewhere in the middle. To add a row at the end of the collection, specify the <code>-1</code> value, or the length of the '''rows''' collection minus <code>1</code>.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>

}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}