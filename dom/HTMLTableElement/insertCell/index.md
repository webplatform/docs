{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=Integer|Description='''Integer''' that specifies where to insert the cell in the '''tr'''. The default value is '''-1''', which appends the new cell to the end of the [[dom/properties/cellSpacing|'''cells''']] collection.|Optional=}}
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Returns the '''td''' element object if successful, or null otherwise.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''insertCell''' method to add a cell to the end of the '''tr'''.
|LiveURL=
|Code=
myNewCell {{=}} document.all.myTable.rows[0].insertCell() 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The preferred technique for inserting a cell is to add the cell at the end of the [[dom/properties/cellSpacing|'''cells''']] collection. It is faster to add a cell at the end of a row than somewhere in the middle. To add a cell at the end of the collection, specify the <code>-1</code> value, or the length of the '''cells''' collection minus <code>1</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>tr</code>
*<code>Reference</code>
*<code>[[dom/methods/deleteCell|deleteCell]]</code>
*<code>[[dom/methods/insertRow|insertRow]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}