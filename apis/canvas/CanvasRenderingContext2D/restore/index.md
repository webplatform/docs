{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Pops the top entry from the drawing state stack, and reset the drawing state it describes. If there is no saved state, the method does nothing.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=Use the ''restore'' method to retrieve a context state previously saved with the [[apis/canvas/CanvasRenderingContext2D/save|save]] method. Affects the following states and attributes:
*The current transformation matrix
*The current clipping region
*The current values of the following attributes:
**''strokeStyle''
**''fillStyle''
**''globalAlpha''
**''lineWidth''
**''lineCap''
**''lineJoin''
**''miterLimit''
**''shadowOffsetX''
**''shadowBlur''
**''shadowColor''
**''globalCompositeOperation''
**''font''
**''textAlign''
**''textBaseline''

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
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}