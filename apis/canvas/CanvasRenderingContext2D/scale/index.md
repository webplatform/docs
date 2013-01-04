{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds the scaling transformation described by the arguments to the transformation matrix. The ''x'' argument represents the scale factor in the horizontal direction; the ''y'' argument represents the scale factor in the vertical direction. The factors are multiples.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The horizontal scaling factor, where 1 equals unity or 100% scale.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The vertical scaling factor.
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
|Notes=When  you create a [[apis/canvas/CanvasRenderingContext2D|CanvasRenderingContext2D]] object, it has a transformation matrix that identifies the current state.  The ''scale'' method  modifies the transformation by multiplying the matrix by the  specified  factor. 

For example, <code>context.scale(1,.5)</code> halves the vertical (or y-axis) values  that are used in context and  leaves  the horizontal (or x-axis) values the same. Similarly, <code>context.scale(2,2)</code>  doubles  the size of the graphics.
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