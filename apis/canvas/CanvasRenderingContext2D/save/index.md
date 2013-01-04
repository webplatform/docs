{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Saves the current state of the context. Use the restore() method to retrieve the saved state.}}
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
|Notes=The ''save'' and [[apis/canvas/CanvasRenderingContext2D/restore|restore]] methods  preserve and restore the state of a context, but not specific paths or graphics. The following attributes and states are affected:
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

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
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