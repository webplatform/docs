{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Modifies the transformation matrix of this context by adding the scaling transformation described by the arguments to the transformation matrix. The arguments represent the scale factors in the horizontal (''x'') and vertical (''y'') directions. The factors are multiples.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=String
|Description=The value to add to horizontal (or x) coordinates.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=The value to add to vertical (or y) coordinates.
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
|Notes=The ''translate'' method  effectively remaps the (0,0)  origin on a canvas.  You can specify one or both parameters. When  you call a canvas method such as  [[apis/canvas/CanvasRenderingContext2D/lineTo|lineTo]], the translate value is added to the respective x-coordinate  and y-coordinate values. ''translate'' does not return an error if either value or any derived value is out of the canvas dimensions.
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