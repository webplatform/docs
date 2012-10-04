{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=m11|Data type=float|Description=The  m'''1,1'''  value in the matrix.|Optional=}}
{{Method Parameter|Name=m12|Data type=float|Description=The  m'''1,2''' value  in the matrix.|Optional=}}
{{Method Parameter|Name=m21|Data type=float|Description=The  m'''2,1'''  value in the matrix.|Optional=}}
{{Method Parameter|Name=m22|Data type=float|Description=The  m'''2,2'''  value in the matrix.|Optional=}}
{{Method Parameter|Name=dx|Data type=float|Description=The delta x (dx)  value in the matrix.|Optional=}}
{{Method Parameter|Name=dy|Data type=float|Description=The  delta y (dy)  value in the matrix.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The parameters of '''transform'''  represent a matrix of the following format.

This matrix is multiplied with the transformation matrix of the current context.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*<code>[[canvas/methods/setTransform|setTransform]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}