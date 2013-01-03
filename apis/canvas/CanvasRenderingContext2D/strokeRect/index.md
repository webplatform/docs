{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Takes the result of tracing the path, using the CanvasRenderingContext2D object's line styles, and fills it with the strokeStyle.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=w
|Data type=Number
|Description=The width, in pixels, of  the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=h
|Data type=Number
|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}
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
|Notes=The ''strokeRect''  method creates a path  that  requires the use of  the [[apis/canvas/CanvasRenderingContext2D/stroke|stroke]]  method to render the rectangle. The outline uses the current [[apis/canvas/CanvasRenderingContext2D/strokeStyle|strokeStyle]], [[apis/canvas/CanvasRenderingContext2D/lineWidth|lineWidth]], [[apis/canvas/CanvasRenderingContext2D/lineJoin|lineJoin]], and, when appropriate, [[apis/canvas/CanvasRenderingContext2D/miterLimit|miterLimit]]  properties. If  the  ''w'' or ''h''  parameter  is zero, a line is drawn. If  the  ''w''  and ''h''  parameters are zero, the rectangle is not drawn.
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